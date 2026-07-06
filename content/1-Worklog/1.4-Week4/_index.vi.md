---
title: "Worklog Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:
- Nghiên cứu sâu về các khái niệm mạng an toàn trong đám mây sử dụng Amazon VPC (Virtual Private Cloud).
- Làm quen với Subnets, Internet Gateways, NAT Gateways, Route Tables và Security Groups.
- Khảo sát mô hình kiến trúc thiết kế ứng dụng Flutter hiện đại và các framework quản lý trạng thái (State Management).
- Chuẩn bị các tiêu chuẩn kết nối mạng để tích hợp ứng dụng di động Flutter đa nền tảng với hệ thống backend từ xa.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Trình bày đề xuất cô lập mạng cho các kết nối khách hàng doanh nghiệp và các dịch vụ tính toán nội bộ phía sau | 11/05/2026 | 11/05/2026 | Văn phòng công ty |
| 3 | - Nghiên cứu giải phẫu cấu trúc của một Amazon VPC: phân tách rõ ràng phân vùng mạng công khai (Public Subnet) và phân vùng mạng bảo mật (Private Subnet) <br> - Thực hành cấu hình danh sách kiểm soát truy cập mạng (NACLs) và các nhóm bảo mật (Security Groups) | 12/05/2026 | 12/05/2026 | https://cloudjourney.awsstudygroup.com/ |
| 4 | - Đánh giá các giải pháp quản lý trạng thái trong Flutter (Bloc, Provider, Riverpod) <br> - Xây dựng một giao diện mockup giao diện đăng ký người dùng với các quy tắc kiểm tra dữ liệu đầu vào | 13/05/2026 | 13/05/2026 | Tài liệu Flutter |
| 5 | - Nghiên cứu mô hình kết nối mạng trong Flutter sử dụng các gói client trừu tượng như `dio` và `http` <br> - Triển khai lớp xử lý ngoại lệ (Exception Handling) ở phía client cho các kịch bản mạng chập chờn | 14/05/2026 | 14/05/2026 | Tài liệu Flutter |
| 6 | - Kiểm thử các tương tác dữ liệu mockup tại local Flutter cùng với các trạng thái dữ liệu giả định <br> - Viết tài liệu quy chuẩn kỹ thuật bảo mật kết nối giữa ứng dụng di động và API Gateway | 15/05/2026 | 15/05/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Kết quả đạt được tuần 4:

#### 1. Cô lập mạng lưới đám mây
* Thiết kế và xây dựng thành công một topo mạng **Amazon VPC**, phân bổ các subnet công khai và riêng tư trên mô hình đa phân vùng sẵn sàng (Multi-AZ).
* Cấu hình các **Security Groups** đóng vai trò tường lửa trạng thái kiểm soát chặt chẽ các luật inbound/outbound, đảm bảo các nút xử lý dữ liệu nhạy cảm hoàn toàn không bị lộ diện ra ngoài Internet công cộng.

#### 2. Kỹ thuật Client-Side & Quy chuẩn kết nối
* Xây dựng thành công bộ khung UI cơ sở có khả năng mở rộng tốt bằng **Flutter**, tích hợp các lớp xác thực định dạng dữ liệu ngay tại màn hình đăng ký.
* Thiết lập các lớp mạng trừu tượng chuẩn hóa sử dụng hệ sinh thái `dio`, chuẩn bị sẵn sàng cho việc nhúng các bộ đánh chặn (Interceptors) token xác thực và kết nối trực tiếp với API thật.