---
title: "Worklog Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:
- Nghiên cứu các dịch vụ tính toán (Compute) và lưu trữ (Storage) cốt lõi của AWS cho mô hình Serverless.
- Làm chủ cơ chế vận hành và vòng đời thực thi (Lifecycle) của AWS Lambda.
- Hiểu rõ kiến trúc Amazon S3, chính sách phân quyền bucket (Bucket Policy) và các mô hình quản lý tài sản số.
- Triển khai các bản thử nghiệm thực tế (Proof-of-Concept - PoC) trực tiếp trên AWS Console.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Tham gia họp kỹ thuật thảo luận về mô hình kiến trúc Microservices so với Serverless cho hệ thống backend BILLO | 27/04/2026 | 27/04/2026 | Văn phòng công ty |
| 3 | - Đi sâu vào cơ chế cốt lõi của AWS Lambda (Execution Context, Cold Start, IAM Execution Role) <br> - Viết và kiểm thử các hàm Lambda Node.js cơ bản trực tiếp trên môi trường mã nguồn của AWS Console | 28/04/2026 | 28/04/2026 | https://cloudjourney.awsstudygroup.com/ |
| 4 | - Nghiên cứu kiến trúc Amazon Simple Storage Service (S3) và các phân lớp lưu trữ (Storage Classes) <br> - Thực hành tạo S3 bucket, tải đối tượng lên và cấu hình quyền truy cập công khai/riêng tư | 29/04/2026 | 29/04/2026 | https://cloudjourney.awsstudygroup.com/ |
| 5 | - Cấu hình các quy tắc bảo mật nâng cao cho S3 Bucket Policies và chia sẻ tài nguyên đa miền (CORS) <br> - Thiết lập cơ chế kích hoạt tự động (Trigger) kết nối một sự kiện tải file lên S3 với một hàm Lambda | 30/04/2026 | 30/04/2026 | https://cloudjourney.awsstudygroup.com/ |
| 6 | - Kiểm thử luồng xử lý hướng sự kiện (Event-driven) bằng cách phân tích log chi tiết sinh ra trong CloudWatch <br> - Tổng hợp tài liệu về đặc tính hiệu năng và các điểm lưu ý đối với hạ tầng lưu trữ serverless | 01/05/2026 | 01/05/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Kết quả đạt được tuần 2:

#### 1. Cơ chế tính toán Serverless
* Làm chủ vòng đời vận hành của **AWS Lambda**, bao gồm các liên kết trigger kích hoạt, cấu hình thời gian chạy tối đa (Timeout) và phân quyền vai trò thực thi.
* Xây dựng thành công các hàm Lambda xử lý dữ liệu đầu vào dạng JSON và trả về các phản hồi có cấu trúc theo chuẩn API.

#### 2. Quản lý lưu trữ đám mây & Kiến trúc hướng sự kiện
* Tiếp thu sâu sắc kiến trúc lưu trữ đối tượng của **Amazon S3**, danh sách kiểm soát truy cập tài nguyên (ACLs) và quyền hạn trên bucket.
* Thiết lập thành công một vòng lặp tự động hướng sự kiện: hành động tải một tệp tin lên đường dẫn S3 được bảo mật sẽ tự động kích hoạt một hàm AWS Lambda xử lý bất đồng bộ ở phía sau.
* Thiết lập cấu hình các quy tắc CORS thắt chặt, ngăn chặn hiệu quả các tên miền client không hợp lệ cố tình gọi đến tài nguyên hệ thống.