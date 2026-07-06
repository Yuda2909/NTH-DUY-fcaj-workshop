---
title: "Worklog Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:
- Nghiên cứu chuyên sâu về kỹ thuật mô hình hóa dữ liệu nâng cao trong Amazon DynamoDB: Single-Table Design.
- Khảo sát Global Secondary Indexes (GSIs) và Local Secondary Indexes (LSIs).
- Ánh xạ các mối quan hệ thực thể phức tạp (Một-nhiều, Nhiều-nhiều) vào trong một bảng NoSQL duy nhất.
- Thiết lập từ điển dữ liệu (Data Dictionary) sơ bộ cho công cụ xử lý cốt lõi của AWS BILLO.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Thảo luận và làm rõ các mối quan hệ dữ liệu của người dùng, đối tác thương mại, cửa hàng vật lý và số dư ví điện tử | 18/05/2026 | 18/05/2026 | Văn phòng công ty |
| 3 | - Nghiên cứu khung lý thuyết thiết kế Single-Table Design được tiên phong bởi các chuyên gia trong ngành <br> - Tìm hiểu cách thức các khóa phân vùng tổng quát (`PK`) và khóa sắp xếp (`SK`) thay thế các bảng riêng lẻ | 19/05/2026 | 19/05/2026 | Tài liệu DynamoDB |
| 4 | - Thiết kế các mô hình truy cập (Access Patterns) để lấy thông tin một cửa hàng, ví người dùng và bộ lọc lịch sử giao dịch <br> - Phác thảo sơ đồ ánh xạ thực thể mối quan hệ trên các công cụ bảng tính | 20/05/2026 | 20/05/2026 | Tài liệu DynamoDB |
| 5 | - Triển khai và cấu hình các Global Secondary Indexes (GSIs) để phục vụ cho các truy vấn đảo ngược thực thể <br> - Phân tích khái niệm quá tải chỉ mục (Index Overloading) nơi một GSI phục vụ nhiều yêu cầu truy vấn khác nhau | 21/05/2026 | 21/05/2026 | Tài liệu DynamoDB |
| 6 | - Trình bày ma trận các mô hình truy cập đã hoàn thiện cho Mentor dự án đánh giá và duyệt kiến trúc <br> - Tối ưu hóa chiến lược phân bổ khóa phân vùng nhằm giảm thiểu rủi ro nghẽn phân vùng (Hot-partition) | 22/05/2026 | 22/05/2026 | Văn phòng công ty |

---

### Kết quả đạt được tuần 5:

#### 1. Chiến lược Single-Table Design
* Làm chủ kỹ thuật nâng cao **Mô hình hóa NoSQL** thông qua tư duy Single-Table Design, chuyển dịch hoàn toàn khỏi tư duy cơ sở dữ liệu quan hệ truyền thống nhằm triệt tiêu chi phí tính toán của các lệnh Join đa bảng.
* Xây dựng tài liệu ma trận hoàn chỉnh đáp ứng hơn 15+ mô hình truy cập (Access Patterns) của ứng dụng, đảm bảo tốc độ truy xuất dữ liệu tối ưu ở mức $O(1)$ hoặc $O(\log N)$.

#### 2. Kỹ thuật Quá tải chỉ mục & An toàn băng thông
* Cấu hình thành công các **Global Secondary Indexes (GSIs)** áp dụng kỹ thuật quá tải từ khóa, cho phép tìm kiếm chéo dữ liệu một cách linh hoạt qua các trường như `StoreId`, `TransactionDate`, hay `MerchantStatus` trong cùng một kho lưu trữ.
* Loại bỏ nguy cơ thắt nút cổ chai dữ liệu bằng cách cấu trúc đồng đều các chiến lược phân phối dữ liệu trên các phân vùng giao dịch có tần suất truy cập cao.