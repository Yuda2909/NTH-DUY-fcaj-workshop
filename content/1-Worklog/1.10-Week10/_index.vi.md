---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:
- Triển khai toàn bộ logic nghiệp vụ cốt lõi cho các phân hệ Khách hàng (Customer) và Đối tác (Merchant).
- Xây dựng quy trình xử lý dữ liệu cho việc xem danh mục cửa hàng, giỏ hàng, thanh toán và các thao tác trên ví.
- Tích hợp lớp kiểm tra dữ liệu đầu vào (Validation Layers) và các pattern middleware bên trong các hàm AWS Lambda.
- Kết nối các màn hình giao diện Flutter hoàn chỉnh với các entrypoint chức năng của backend.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Thực hiện rà soát mã nguồn (Code Review) cho các hàm lõi ban đầu và thống nhất các thư viện kiểm tra dữ liệu đầu vào | 22/06/2026 | 22/06/2026 | Văn phòng công ty |
| 3 | - Viết các phương thức xử lý trong Lambda cho việc xác thực hồ sơ Merchant và cấu hình thông tin Cửa hàng <br> - Triển khai các câu lệnh truy vấn kiểm tra trạng thái hoạt động trực tiếp trong DynamoDB | 23/06/2026 | 23/06/2026 | Node.js & AWS SDK |
| 4 | - Triển khai logic tạo Đơn hàng cho Khách hàng bao gồm các công thức tính toán giá và kiểm tra tồn kho <br> - Viết các tiến trình cập nhật số dư ví điện tử đảm bảo tính nguyên tử (Atomic updates) | 24/06/2026 | 24/06/2026 | Node.js & AWS SDK |
| 5 | - Tối ưu hóa các dịch vụ kết nối mạng trong Flutter để bắt các mã lỗi API chuẩn và hiển thị thông báo tường minh lên giao diện <br> - Đồng bộ thông tin hồ sơ người dùng vào bộ lưu trữ trạng thái local | 25/06/2026 | 25/06/2026 | Tài liệu Flutter |
| 6 | - Kiểm thử luồng thanh toán và hoàn tất đơn hàng trực tiếp với các endpoint thật trên môi trường dev <br> - Triển khai cơ chế lưu bộ nhớ đệm (Local Caching) trên Flutter cho các tài sản cửa hàng tĩnh | 26/06/2026 | 26/06/2026 | Tài liệu Flutter |

---

### Kết quả đạt được tuần 10:

#### 1. Hoàn thiện Logic Nghiệp vụ Cốt lõi
* Xây dựng các module backend tối ưu bằng **Node.js và AWS SDK v3** để xử lý mượt mà việc tạo hồ sơ merchant, quản lý danh mục sản phẩm và hiển thị thông tin cửa hàng.
* Thiết kế các tiến trình giao dịch bảo mật cho việc đặt hàng, tận dụng các ràng buộc cấu trúc của DynamoDB nhằm triệt tiêu hoàn toàn rủi ro sai lệch số dư tài khoản khi có tranh chấp dữ liệu đồng thời.

#### 2. Nâng cao Khả năng Kết nối của Client
* Liên kết các trạng thái UI phức tạp trong **Flutter** trực tiếp với phản hồi từ server thực tế, loại bỏ hoàn toàn hiện tượng bất đồng bộ hoặc treo màn hình khi kết nối mạng kém.
* Triển khai thành công cơ chế lưu bộ nhớ đệm local cho các mảng dữ liệu hình ảnh cửa hàng, giúp giảm đáng kể số lượng request tải lại tài sản trùng lặp từ Amazon S3, tối ưu băng thông cho client.