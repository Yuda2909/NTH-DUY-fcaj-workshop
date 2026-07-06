---
title: "Worklog Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:
- Hoàn thiện sơ đồ kiến trúc tổng thể cốt lõi cho môi trường phát triển dự án AWS BILLO.
- Thiết lập các đặc tả giao tiếp chuẩn hóa giữa các thành phần hệ thống (API Contracts).
- Khởi tạo các kho lưu trữ mã nguồn khung (Boilerplate Repositories) và thống nhất các pattern viết code sạch.
- Hoàn tất toàn bộ các điều kiện tiên quyết trước khi bước vào giai đoạn code hệ thống trên diện rộng.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Thống nhất và chốt sơ đồ kiến trúc hệ thống tổng thể với các kỹ sư trưởng của dự án | 08/06/2026 | 08/06/2026 | Văn phòng công ty |
| 3 | - Soạn thảo chi tiết các endpoint API, cấu trúc request schema, mã trạng thái phản hồi và dữ liệu mẫu qua chuẩn OpenAPI/Swagger | 09/06/2026 | 09/06/2026 | Tài liệu nội bộ |
| 4 | - Đánh giá các giải pháp đảm bảo an toàn giao dịch tài chính thông qua cơ chế thử lại (API Retries) và tầng kiểm soát trùng lặp dữ liệu (Idempotency) <br> - Phân định quyền hạn cho từng cụm Lambda truy cập vào các phân vùng dữ liệu riêng biệt | 10/06/2026 | 10/06/2026 | Tài liệu nội bộ |
| 5 | - Quy định cấu trúc tổ chức code mã nguồn cho Node.js backend (Layered Architecture: Controller-Service-Repository) <br> - Quy định cấu trúc thư mục cho dự án Flutter (phương pháp tiếp cận Feature-first hoặc Layer-first) | 11/06/2026 | 11/06/2026 | Sách hướng dẫn Flutter & Node.js |
| 6 | - Đóng gói toàn bộ tài liệu kiến trúc, sơ đồ mạng lưới và từ điển dữ liệu vào không gian tri thức chung của nhóm (Wiki) <br> - Rà soát lại mức độ sẵn sàng của các tài khoản cloud trước khi bước vào sprint code | 12/06/2026 | 12/06/2026 | Văn phòng công ty |

---

### Kết quả đạt được tuần 8:

#### 1. Hoàn thiện thiết kế hệ thống tổng thể
* Hoàn thành sơ đồ thiết kế hệ thống nhiều lớp cho hệ sinh thái **AWS BILLO**, xác định rõ ràng ranh giới cô lập giữa các thành phần client và hệ thống xử lý backend.
* Viết thành công bộ **Hợp đồng API (API Contracts) theo chuẩn OpenAPI/Swagger**, triệt tiêu hoàn toàn các rủi ro không khớp dữ liệu giữa các lập trình viên làm client-side và data controller.

#### 2. Đồng bộ Pattern thiết kế & Cấu trúc mã nguồn
* Thống nhất thành công kiến trúc mã nguồn sạch cho toàn dự án (Mô hình Controller-Service-Repository cho các module backend; phân tách theo Tính năng - Feature-driven cho các thư mục mã nguồn Flutter).
* Tài liệu hóa thành công giải pháp kỹ thuật cụ thể cho việc xử lý an toàn tài chính, áp dụng cơ chế băm chuỗi token (Request Hashing) độc nhất để ép hệ thống tuân thủ tính nhất quán (Idempotency).