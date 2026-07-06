---
title: "Worklog Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:
- Tiếp cận nền tảng cơ sở dữ liệu NoSQL với trọng tâm là Amazon DynamoDB.
- Khảo sát các khái niệm nền tảng của DynamoDB: Partition Key (PK), Sort Key (SK) và các loại Index.
- Nghiên cứu kiến trúc thiết kế API thông qua cổng kết nối Amazon API Gateway.
- Xây dựng một đường ống tích hợp backend hoàn chỉnh: API Gateway sang Lambda sang DynamoDB.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Đồng bộ yêu cầu về tầng lưu trữ dữ liệu cho hệ thống sổ cái BILLO và nhu cầu xử lý giao dịch thời gian thực | 04/05/2026 | 04/05/2026 | Văn phòng công ty |
| 3 | - Tìm hiểu mô hình dữ liệu DynamoDB, đơn vị năng suất Đọc/Ghi (RCU/WCU) và cơ chế tính giá theo nhu cầu (On-demand) <br> - Thực hành tạo các bảng thử nghiệm sử dụng khóa chính hỗn hợp (Composite Primary Key: PK + SK) | 05/05/2026 | 05/05/2026 | https://cloudjourney.awsstudygroup.com/ |
| 4 | - Nghiên cứu Amazon API Gateway (so sánh tính năng REST APIs và HTTP APIs) <br> - Thiết kế các endpoint HTTP đơn giản, các đường dẫn (paths), tham số truy vấn và sơ đồ phương thức (GET/POST) | 06/05/2026 | 06/05/2026 | https://cloudjourney.awsstudygroup.com/ |
| 5 | - Cấu hình định tuyến trên API Gateway để làm proxy chuyển tiếp trực tiếp traffic mạng vào một hàm Lambda <br> - Phân quyền vai trò IAM cấp phép cho hàm Lambda đọc và ghi bản ghi vào bảng DynamoDB | 07/05/2026 | 07/05/2026 | https://cloudjourney.awsstudygroup.com/ |
| 6 | - Thực hiện kiểm thử endpoint toàn diện đầu cuối (End-to-End) thông qua các công cụ kiểm thử API (Postman) <br> - Phân tích thời gian thực thi luồng dữ liệu và thống kê các chỉ số về băng thông ban đầu | 08/05/2026 | 08/05/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Kết quả đạt được tuần 3:

#### 1. Kiến trúc NoSQL được quản trị hoàn toàn
* Thành thạo mô hình cấp phát dữ liệu của **Amazon DynamoDB**, cấu trúc của phần tử (Item) và các kiểu dữ liệu tương thích.
* Tạo lập thành công các bảng dữ liệu schema-less tận dụng khóa chính hỗn hợp, cho phép thực hiện các truy vấn dữ liệu đa chiều – điều kiện bắt buộc để quản lý lịch sử giao dịch sau này.

#### 2. Tích hợp đồng bộ chuẩn RESTful
* Hiệu chỉnh và làm chủ cơ chế vận hành của **Amazon API Gateway**, cấu trúc chuyển đổi request đầu vào (Integration Mapping) và ghi đè trạng thái mã lỗi HTTP.
* Triển khai thành công một đường ống serverless 3 lớp hoàn chỉnh: Cổng API Gateway tiếp nhận các request HTTP từ client bên ngoài, ủy quyền dữ liệu an toàn vào hàm tính toán Lambda, hàm này sau đó xử lý logic và trực tiếp ghi/đọc dữ liệu vào kho lưu trữ DynamoDB.