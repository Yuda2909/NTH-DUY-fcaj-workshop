---
title: "Worklog Tuần 1"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu tuần 1:
- Kết nối, làm quen với các thành viên trong nhóm nội bộ và Mentor hướng dẫn dự án.
- Nắm rõ các quy định làm việc, giao thức bảo mật và quy trình vận hành của công ty.
- Nghiên cứu tài liệu tổng quan ban đầu (Project Brief) của nền tảng AWS BILLO.
- Khởi tạo môi trường phát triển tại local, bao gồm các công cụ lập trình và giao diện đám mây cơ bản.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty, gặp gỡ các thành viên và Mentor dự án <br> - Đọc và ký kết các quy định nội bộ, thỏa thuận bảo mật (NDA) và chính sách tuân thủ an toàn thông tin | 20/04/2026 | 20/04/2026 | Văn phòng công ty |
| 3 | - Tiếp cận kho lưu trữ mã nguồn (Repository) và đọc tài liệu yêu cầu hệ thống ban đầu của AWS BILLO <br> - Nghiên cứu đối tượng người dùng mục tiêu (Customer, Merchant) và các luồng nghiệp vụ cốt lõi | 21/04/2026 | 21/04/2026 | Tài liệu nội bộ |
| 4 | - Tạo tài khoản AWS Free Tier dành riêng cho việc phát triển cá nhân và thử nghiệm sandbox <br> - Cài đặt và cấu hình AWS Command Line Interface (CLI) trên máy tính cá nhân | 22/04/2026 | 22/04/2026 | https://cloudjourney.awsstudygroup.com/ |
| 5 | - Khởi tạo không gian làm việc local, cài đặt các tài nguyên phụ thuộc (Flutter SDK, Node.js runtime, Git, VS Code) <br> - Kiểm thử việc tạo người dùng IAM với quyền quản trị và quyền truy cập lập trình (Programmatic Access) | 23/04/2026 | 23/04/2026 | https://cloudjourney.awsstudygroup.com/ |
| 6 | - Xác thực thông tin cấu hình local bằng cách chạy các lệnh kiểm tra cơ bản trên AWS CLI <br> - Tài liệu hóa tài liệu hướng dẫn cấu hình môi trường để đồng bộ hóa trong nhóm | 24/04/2026 | 24/04/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Kết quả đạt được tuần 1:

#### 1. Hòa nhập văn hóa & Quy trình làm việc
* Tích hợp thành công vào đội ngũ kỹ thuật và thiết lập kênh giao tiếp rõ ràng với Mentor hướng dẫn dự án.
* Hiểu rõ các tiêu chuẩn quản lý mã nguồn, quy trình vận hành nội bộ và các yêu cầu bảo mật an ninh mạng của công ty.

#### 2. Thiết lập công cụ & Môi trường điện toán đám mây
* Khởi tạo thành công không gian làm việc AWS Free Tier với các thông tin xác thực IAM được phân quyền chặt chẽ, tuân thủ nguyên tắc đặc quyền tối thiểu (PoLP).
* Cài đặt và xác thực thành công môi trường AWS CLI v2 trên máy local với:
    * Liên kết thành công bộ mã `Access Key ID` và `Secret Access Key`.
    * Chỉ định phân vùng mặc định hướng tới region Singapore (`ap-southeast-1`).
* Setup sạch sẽ không gian máy tính cá nhân gồm Flutter SDK (nhánh stable) và Node.js LTS, đảm bảo các runtime đồng bộ với môi trường production sau này.