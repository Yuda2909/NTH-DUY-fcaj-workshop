---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:
- Bắt đầu xây dựng nền tảng cho dự án AWS BILLO.
- Khởi tạo cấu trúc frontend và backend ban đầu.
- Tạo hạ tầng serverless cốt lõi trên AWS cho môi trường phát triển.
- Cấu hình các dịch vụ xác thực, API, cơ sở dữ liệu, lưu trữ và ghi log.
- Triển khai backend ban đầu và kết nối frontend với API thật trên AWS.
- Làm việc trực tiếp tại văn phòng công ty vào ngày 15/06/2026 từ 08:30 đến 16:30.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty từ 08:30 đến 16:30 <br> - Xem lại thiết kế hệ thống ở tuần 8 <br> - Khởi tạo cấu trúc dự án Flutter frontend <br> - Khởi tạo cấu trúc dự án Node.js backend <br> - Trao đổi về cách tổ chức mã nguồn và quy trình phát triển | 15/06/2026 | 15/06/2026 | Văn phòng công ty |
| 3 | - Tạo AWS SAM/CloudFormation template ban đầu <br> - Định nghĩa các tài nguyên serverless cơ bản cho môi trường dev <br> - Chuẩn bị cấu hình triển khai tại region Singapore <br> - Ôn lại mối liên hệ giữa Lambda, API Gateway, DynamoDB và S3 | 16/06/2026 | 16/06/2026 | https://cloudjourney.awsstudygroup.com/ |
| 4 | - Tạo và cấu hình Amazon Cognito User Pool <br> - Tạo các group cho các vai trò trong hệ thống: <br>&emsp; + Customer <br>&emsp; + Merchant <br>&emsp; + Admin <br> - Cấu hình đăng ký bằng số điện thoại và xác thực OTP <br> - Cấu hình API Gateway JWT Authorizer | 17/06/2026 | 17/06/2026 | https://cloudjourney.awsstudygroup.com/ |
| 5 | - Thiết kế và tạo các bảng DynamoDB: <br>&emsp; + Main Table <br>&emsp; + Idempotency Table <br> - Thiết kế mô hình dữ liệu cho profile, wallet, merchant, store, product, order và transaction <br> - Tạo S3 bucket để lưu hình ảnh và giấy phép kinh doanh | 18/06/2026 | 18/06/2026 | https://cloudjourney.awsstudygroup.com/ |
| 6 | - Tạo các Lambda function ban đầu cho logic nghiệp vụ cốt lõi <br> - Xây dựng luồng pre-signed URL để upload trực tiếp lên S3 <br> - Cấu hình CloudWatch Logs cho Lambda function <br> - Deploy stack dev lên AWS <br> - Kết nối Flutter frontend với API thật và kiểm thử request cơ bản | 19/06/2026 | 19/06/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Kết quả đạt được tuần 9:

#### 1. Khởi tạo Dự án & Đồng bộ Kiến trúc
* Đã khởi tạo nền tảng ban đầu cho dự án **AWS BILLO**, tách biệt hoàn toàn ứng dụng client-side với hệ thống backend serverless phía sau.
* Thiết lập một cấu trúc **Flutter frontend chuẩn chỉnh**, sẵn sàng cho sản xuất, áp dụng các kiến trúc quản lý trạng thái và phân bổ thư mục tối ưu cho việc mở rộng quy mô.
* Khởi tạo dự án **Node.js serverless backend**, cấu hình sẵn để phát triển theo hướng microservices tận dụng các tích hợp gốc của AWS.
* Hoàn thành ngày làm việc trực tiếp tại văn phòng để xem lại thiết kế hệ thống của Tuần 8, thống nhất chiến lược phân nhánh Git và các quy chuẩn viết code trong đội ngũ.

#### 2. Hạ tầng dạng mã (IaC) & Cấu hình Môi trường Dev
* Làm chủ việc sử dụng **AWS SAM (Serverless Application Model)** và CloudFormation để định nghĩa các tài nguyên đám mây một cách lập trình.
* Triển khai thành công các cấu hình môi trường hướng tới **region Singapore (`ap-southeast-1`)** để giảm thiểu tối đa độ trễ cho người dùng cuối.
* Đi sâu vào kiến thức kỹ thuật liên quan đến các vòng lặp phản hồi, mô hình kích hoạt (Invocation Patterns) và cơ chế bàn giao ngữ cảnh thực thi giữa API Gateway, Lambda, DynamoDB và S3.

#### 3. Quản lý Định danh & Thực thi Bảo mật
* Tạo và tối ưu hóa một **Amazon Cognito User Pool** đóng vai trò là Nhà cung cấp định danh tập trung (Identity Provider - IdP) cho nền tảng.
* Cấu hình cơ chế phân quyền dựa trên vai trò (RBAC) chặt chẽ bằng cách thiết lập các nhóm người dùng riêng biệt:
    * **Customer**: Dành cho người dùng phổ thông và chủ tài khoản ví.
    * **Merchant**: Dành cho các chủ doanh nghiệp/hộ kinh doanh quản lý gian hàng.
    * **Admin**: Phục vụ các hoạt động vận hành hệ thống nội bộ và phê duyệt hồ sơ.
* Triển khai luồng xác thực bảo mật tận dụng thuộc tính **Số điện thoại và xác thực OTP qua tin nhắn SMS**.
* Bảo vệ các endpoint API bằng cách gắn **API Gateway JWT Authorizer**, ép buộc xác thực chữ ký mã token và kiểm tra tính hợp lệ trên mọi request gửi tới.

#### 4. Mô hình hóa Cơ sở dữ liệu & Cấp phát Lưu trữ đám mây
* Khởi tạo các bảng **Amazon DynamoDB** hiệu năng cao, tối ưu độ trễ cho môi trường serverless:
    * **Main Table**: Tối ưu hóa cho các bản ghi giao dịch áp dụng mô hình Single-Table Design.
    * **Idempotency Table**: Chuyên dụng để ngăn chặn việc xử lý trùng lặp các lệnh gọi API liên quan đến tài chính.
* Hoàn thành sơ đồ mô hình hóa dữ liệu cho các thực thể quan trọng bao gồm: Hồ sơ người dùng, Ví điện tử, Hồ sơ đăng ký merchant, Cửa hàng, Danh mục sản phẩm, Đơn hàng và Giao dịch sổ cái.
* Tạo các **Amazon S3 Buckets** được cấu hình chính sách CORS nghiêm ngặt để lưu trữ hình ảnh sản phẩm và tài liệu KYC doanh nghiệp một cách an toàn.

#### 5. Triển khai Serverless & Tích hợp Frontend
* Phát triển và triển khai các hàm **AWS Lambda cốt lõi** viết bằng Node.js để xử lý các thao tác CRUD cơ sở và kiểm tra phân quyền hệ thống.
* Xây dựng luồng **Tạo Pre-signed URL trên S3**, cho phép frontend tải các tài sản truyền thông dung lượng lớn trực tiếp lên cloud storage một cách an toàn, tránh gây nghẽn cổ chai tại lớp tính toán backend.
* Cấu hình các **Amazon CloudWatch Log Groups** chuyên dụng, hỗ trợ ghi log có cấu trúc để phục vụ việc truy vết thời gian thực, giám sát số liệu hệ thống và gỡ lỗi nhanh chóng.
* Triển khai thành công toàn bộ stack serverless lên môi trường dev thông qua bộ công cụ AWS SAM CLI.
* Kết nối thành công ứng dụng Flutter local với API Gateway thật trên AWS, hoàn thành các bài kiểm tra tích hợp đầu cuối cho các HTTP request có xác thực.