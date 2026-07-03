---
title: "Monitoring and Cleanup"
date: 2026-06-29
weight: 8
chapter: false
pre: " <b> 5.8. </b> "
---

---

This section explains how to monitor the AWS BILLO backend and clean up AWS resources after finishing the workshop.

Monitoring is important because the backend runs on serverless services such as API Gateway, Lambda, DynamoDB, S3, and Cognito. When an error occurs, CloudWatch Logs and AWS Console can help identify the cause.

Cleanup is also important to avoid unnecessary AWS costs after testing.

---

## 1. Monitoring with CloudWatch Logs

AWS BILLO uses Amazon CloudWatch Logs to monitor backend behavior and debug Lambda/API issues.

CloudWatch Logs can help check:

- Lambda execution results.
- API request errors.
- Authentication problems.
- DynamoDB read/write errors.
- S3 upload issues.
- Payment and transaction errors.
- Business registration workflow errors.

---

## Step 1: Open CloudWatch Logs

Open the AWS Management Console and go to:

```text id="5bv8be"
CloudWatch > Logs > Log groups
```
![CloudWatch Logs](/images/5-Workshop/cloudwatch-logs.png)
Search for log groups related to the AWS BILLO Lambda functions.

Lambda log groups usually follow this format:

```text id="nh9kou"
/aws/lambda/<function-name>
```

---

## Step 2: Open a Lambda Log Group

Select a Lambda log group.

Then open the latest log stream.

A log stream usually contains information such as:

```text id="xl6egg"
START RequestId
Function logs
Error messages
END RequestId
REPORT RequestId
```

These logs can be used to check whether a Lambda function executed successfully or failed.

---

## Step 3: Debug API Errors

If the frontend receives an API error, check the related Lambda logs in CloudWatch.

Common API issues include:

| Issue                       | Possible Cause                                       |
| --------------------------- | ---------------------------------------------------- |
| `401 Unauthorized`          | Missing, expired, or invalid JWT token               |
| `403 Forbidden`             | User does not have the required role                 |
| `400 Bad Request`           | Missing or invalid request data                      |
| `404 Not Found`             | Wrong API path or missing record                     |
| `500 Internal Server Error` | Lambda error, DynamoDB error, or unhandled exception |

When debugging, check:

- API Gateway endpoint.
- Request payload.
- JWT token.
- Lambda function logs.
- DynamoDB table records.
- User role in Cognito.

---

## Step 4: Check DynamoDB Data

Open:

```text id="n1c8z9"
DynamoDB > Tables > wallet-app-main-dev
```
<img src="/images/maindev.png" alt="AWS dynamoDB-Tables - Maindev" width="1300">

Check whether expected records exist after running the demo.

Important records may include:

- User profile.
- Wallet.
- Merchant application.
- Store.
- Product or service.
- Table.
- Order.
- Bill.
- Payment session.
- Transaction.

If a feature does not work correctly, compare the expected data with the actual records in DynamoDB.

---

## Step 5: Check S3 Uploads

Open:

```text id="bbmyaz"
Amazon S3 > Buckets
```

Find the upload bucket created by the backend stack.

Check uploaded files such as:

- Business registration documents.
- Store images.
- Product or service images.

If an upload fails, check:

- Whether the pre-signed URL was generated successfully.
- S3 bucket permissions.
- File type and file size.
- Browser console errors.
- Lambda logs in CloudWatch.

---

## Step 6: Check Cognito Users and Groups

Open:

```text id="0ct1l5"
Amazon Cognito > User pools > Users
```
<img src="/images/c-user.png" alt="Amazon Cognito > User pools > Users" width="1300">

Check the user account created during the demo.

Verify:

- User exists.
- User status is confirmed.
- Phone number is correct.
- User belongs to the correct group.

For approved merchants, check that the user has been added to:

```text id="mny5kq"
Merchant
```

For Admin accounts, check that the user belongs to:

```text id="d1v4yq"
Admin
```

---

## Step 7: Check CloudFormation Stack

Open:

```text id="q82d9j"
CloudFormation > Stacks
```

Find the stack:

```text id="aufmnq"
wallet-app-backend-dev
```

Check the stack status.

Expected successful statuses include:

```text id="2mmgf0"
CREATE_COMPLETE
UPDATE_COMPLETE
```
<img src="/images/stack.png" alt="CloudFormation > Stacks" width="1300">


If the stack failed during deployment, open the **Events** tab and review the failed resource.

---

## 2. Cleanup AWS Resources

After finishing the workshop, delete the deployed backend resources if they are no longer needed.

Because the backend was deployed using AWS SAM, cleanup can be done using SAM or CloudFormation.

---

## Option 1: Delete Resources Using SAM

Open PowerShell and go to the backend folder:

```powershell id="u5ay6v"
cd C:\Users\admin\source\repos\AWS_BILLO\backend
```

Run:

```powershell id="75vxmb"
sam delete
```

SAM will ask for confirmation before deleting the stack.

Expected result:

- The CloudFormation stack is deleted.
- Resources managed by the stack are removed.
- Backend resources such as Lambda, API Gateway, DynamoDB, S3, and Cognito may be deleted depending on the stack configuration.

---

## Option 2: Delete Stack from AWS Console

Open:

```text id="8h4s7f"
CloudFormation > Stacks
```

Select:

```text id="dnh9bp"
wallet-app-backend-dev
```

Choose:

```text id="13h4c5"
Delete
```
<img src="/images/delete.png" alt="Delete" width="1300">

Confirm the deletion.

Expected result:

- CloudFormation starts deleting the stack.
- Stack status changes to `DELETE_IN_PROGRESS`.
- When complete, the stack is removed.

---

## Important Cleanup Notes

Before deleting resources, make sure you do not need the test data anymore.

Some resources may contain important demo data, such as:

- User accounts in Cognito.
- Wallet and transaction records in DynamoDB.
- Business documents and product images in S3.
- Lambda logs in CloudWatch.

If the project is still being developed, do not delete the backend stack. Instead, only clean up unused test data.

---

## Optional: Clean Up Test Data Only

If you want to keep the backend but remove test data, manually review and delete test records from:

```text id="gp4rj0"
DynamoDB > Tables > wallet-app-main-dev
```

You can also delete uploaded test files from:

```text id="r6fg34"
Amazon S3 > Buckets
```

Be careful when deleting data because it may affect existing demo users and test flows.

---

## Optional: Control CloudWatch Log Costs

CloudWatch Logs may continue to store logs after testing.

To reduce cost, configure log retention:

```text id="i2g5l9"
CloudWatch > Logs > Log groups > Select log group > Retention settings
```
<img src="/images/rent.png" alt="rentetion" width="1300">


Recommended retention for development:

```text id="pqcdfx"
7 days
14 days
30 days
```
<img src="/images/setting.png" alt="rentetion" width="900">



Avoid keeping development logs forever if they are not needed.

---

## Optional: Set AWS Budget Alert

To avoid unexpected AWS costs, configure an AWS Budget alert.

Open:

```text id="uz7wul"
Billing and Cost Management > Budgets
```

Create a monthly cost budget.

Example:

```text id="1687ow"
Budget amount: 5 USD
Alert threshold: 80%
Email notification: your email address
```

This helps detect unexpected costs from services such as SMS, CloudWatch Logs, S3 storage, or API usage.

---

## Common Cleanup Issues

### Stack deletion fails

Possible causes:

- S3 bucket is not empty.
- DynamoDB table has deletion protection.
- IAM permission is missing.
- A resource was modified manually outside CloudFormation.

Check CloudFormation Events to identify the failed resource.

### S3 bucket cannot be deleted

If the bucket is not empty, delete objects inside the bucket first.

Then run `sam delete` again or delete the stack from CloudFormation.

### Resources still appear after deletion

Some resources may take several minutes to disappear from the console.

Refresh the AWS Console and check CloudFormation stack events.

---

## Expected Result

After completing this section:

- Lambda logs can be checked in CloudWatch.
- Data can be verified in DynamoDB.
- Uploads can be checked in S3.
- Users and groups can be checked in Cognito.
- The backend stack can be deleted using SAM or CloudFormation.
- Unnecessary AWS costs can be reduced after the workshop.
