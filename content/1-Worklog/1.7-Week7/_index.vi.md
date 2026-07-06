---
title: "Worklog Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:
- Nghiên cứu kiến trúc quản lý định danh người dùng, dịch vụ thư mục liên kết và vòng đời của mã token bảo mật.
- Tìm hiểu sâu về dịch vụ Amazon Cognito User Pools và Amazon Cognito Identity Pools.
- Lên sơ đồ yêu cầu bảo mật đa người thuê (Multi-tenant) và quy trình đăng ký tài khoản cho AWS BILLO.
- Tìm hiểu chuẩn xác thực OAuth 2.0 và quy trình xác minh chữ ký mã token JSON Web Token (JWT).

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Tham gia các buổi đánh giá cấu trúc về bảo mật truy cập, thời gian hết hạn phiên làm việc và thuộc tính tùy chỉnh (Custom Attributes) | 01/06/2026 | 01/06/2026 | Văn phòng công ty |
| 3 | - Nghiên cứu sâu cấu hình của Amazon Cognito User Pools: thuộc tính người dùng, chính sách mật khẩu phức tạp và cấu hình MFA | 02/06/2026 | 02/06/2026 | Tài liệu Cognito |
| 4 | - Phân tích các luồng xác thực tùy chỉnh nâng cao (Define Auth Challenge, Create Auth Challenge, Verify Auth Challenge Response) | 03/06/2026 | 03/06/2026 | Tài liệu Cognito |
| 5 | - Học cách nhúng các thông tin phân quyền tùy chỉnh (Custom Claims) vào trong mã JWT Access Token phục vụ phân quyền <br> - Tìm hiểu giải phẫu một mã token, cơ chế xác thực chữ ký số dựa trên các endpoint JWKS công khai | 04/06/2026 | 04/06/2026 | Tài liệu Cognito |
| 6 | - Xây dựng sơ đồ tuần tự (Sequence Diagram) mô tả các trạng thái đăng ký và xác thực cho khách hàng và đối tác <br> - Thảo luận và thống nhất phương án thiết kế hệ thống định danh với Technical Lead | 05/06/2026 | 05/06/2026 | Văn phòng công ty |

---

### Kết quả đạt được tuần 7:

#### 1. Kiến trúc quản lý định danh chuyên nghiệp
* Tiếp thu kiến thức nâng cao về **Amazon Cognito**, tập trung vào việc đăng ký tài khoản an toàn, phân tách dữ liệu người dùng và các thao tác đăng nhập không mật khẩu.
* Xây dựng thành công các sơ đồ logic cho luồng đăng nhập bằng số điện thoại, sử dụng mã OTP qua tin nhắn SMS thông qua việc cấu hình các thử thách xác thực tùy chỉnh (Custom Auth Challenges).

#### 2. Khung bảo mật dựa trên Token (Token-Based)
* Làm chủ cấu trúc các loại mã **JSON Web Token (JWT)** gồm `id_token`, `access_token`, và `refresh_token`, bao gồm cả các quy trình kiểm tra chữ ký mật mã học.
* Thiết kế thành công cấu trúc dữ liệu nhúng các phân quyền vai trò (Access Claims) vào token, tạo tiền đề cho việc phân quyền dựa trên vai trò (RBAC) một cách gọn nhẹ, mượt mà.