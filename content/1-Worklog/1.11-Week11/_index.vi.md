---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:
- Thiết lập một đường ống triển khai tự động liên tục (CI/CD Pipeline) cho ứng dụng serverless.
- Khai báo các kịch bản chạy tự động (Pipeline Definitions) trong nền tảng GitHub Actions.
- Xây dựng hệ thống kiểm thử tự động (Unit Testing) cho các hàm backend và ứng dụng khách.
- Cấu hình các biến môi trường chuyên biệt, phân tách rõ ràng phạm vi chạy giữa môi trường Production và Development.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Thiết kế mô hình bảo mật cho đường ống deploy tự động cùng với Kỹ sư trưởng | 29/06/2026 | 29/06/2026 | Văn phòng công ty |
| 3 | - Thiết lập các bộ công cụ chạy unit test (Jest cho các module Node.js; công cụ test gốc của Flutter cho client) <br> - Viết các kịch bản kiểm tra logic tính toán cho các hàm xử lý dòng tiền | 30/06/2026 | 30/06/2026 | Jest & Flutter Docs |
| 4 | - Viết tệp tin khai báo quy trình tự động (`.github/workflows/deploy.yml`) <br> - Cấu hình các bước kiểm tra chuẩn viết code (Linting), chạy test tự động và build mã nguồn | 01/07/2026 | 01/07/2026 | Sách hướng dẫn GitHub Actions |
| 5 | - Thiết lập cơ chế định danh OpenID Connect (OIDC) để cấp quyền cho GitHub truy cập an toàn vào AWS mà không cần lưu Access Key tĩnh <br> - Tự động hóa việc deploy stack lên nhiều môi trường | 02/07/2026 | 02/07/2026 | Sách hướng dẫn Bảo mật AWS |
| 6 | - Chạy thử nghiệm toàn diện luồng Tích hợp liên tục bằng cách tạo các sự kiện merge code trên Git <br> - Kiểm tra nhật ký chạy (Logs) của pipeline để tối ưu thời gian build | 03/07/2026 | 03/07/2026 | Sách hướng dẫn GitHub Actions |

---

### Kết quả đạt được tuần 11:

#### 1. Tự động hóa Quy trình Phát triển (CI/CD)
* Xây dựng thành công hệ thống **CI/CD hoàn chỉnh sử dụng GitHub Actions**, loại bỏ hoàn toàn việc deploy thủ công bằng tay vốn tiềm ẩn nhiều sai sót lên đám mây.
* Thắt chặt an toàn thông tin cho hệ thống bằng việc cấu hình **trao đổi token OIDC**, loại bỏ hoàn toàn việc phải lưu trữ các khóa bí mật AWS root dài hạn trên các hệ thống của bên thứ ba.

#### 2. Đảm bảo Chất lượng & Kiểm thử Nghiêm ngặt
* Ép buộc quy trình chạy kiểm thử tự động (Automated Unit Tests) đối với mọi yêu cầu thay đổi mã nguồn (Pull Request), đảm bảo code mới không làm hỏng các tính năng cũ.
* Thiết lập các môi trường staging độc lập (`dev`, `staging`), tạo không gian an toàn để nghiệm thu tính năng mới trước khi đưa lên production.