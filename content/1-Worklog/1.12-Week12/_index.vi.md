---
title: "Worklog Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:
- Thực hiện kiểm thử tích hợp (Integration Test) toàn diện trên toàn bộ các giao diện hệ thống.
- Tiến hành đánh giá hiệu năng chịu tải (Load Testing) và kiểm tra lỗ hổng bảo mật bằng các công cụ chuyên dụng.
- Thống kê dữ liệu, xây dựng bảng biểu phân tích chi phí tiêu thụ tài nguyên đám mây của hạ tầng serverless.
- Hoàn thiện tài liệu báo cáo thực tập/dự án cuối khóa và thuyết trình kết quả trước hội đồng công ty.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Thiết lập các kịch bản kiểm thử chéo hệ thống trên các thiết bị di động vật lý kết nối với backend thật | 06/07/2026 | 06/07/2026 | Văn phòng công ty |
| 3 | - Đo đạc hiệu năng các chỉ mục tìm kiếm trên DynamoDB và giám sát hiện tượng Cold Start của Lambda thông qua AWS X-Ray <br> - Áp dụng các tinh chỉnh tối ưu hóa mã nguồn | 07/07/2026 | 07/07/2026 | AWS CloudWatch & X-Ray |
| 4 | - Trích xuất dữ liệu chi phí vận hành tài nguyên cloud từ giao diện AWS Cost Explorer <br> - Phác thảo báo cáo dự phóng ngân sách hoạt động khi ứng dụng tăng trưởng quy mô lớn | 08/07/2026 | 08/07/2026 | AWS Billing Console |
| 5 | - Dọn dẹp các stack cloud thử nghiệm không còn sử dụng và thu hẹp các chính sách phân quyền IAM <br> - Tổng hợp tài liệu hướng dẫn vận hành và sơ đồ hệ thống vào không gian lưu trữ chung | 09/07/2026 | 09/07/2026 | Tài liệu nội bộ |
| 6 | - Báo cáo, thuyết trình đồ án kỹ thuật AWS BILLO trước Mentor và Hội đồng Công nghệ của công ty <br> - Hoàn tất các thủ tục đánh giá kết quả thực tập và bàn giao thiết bị | 10/07/2026 | 10/07/2026 | Văn phòng công ty |

---

### Kết quả đạt được tuần 12:

#### 1. Tối ưu hóa Hệ thống Toàn diện
* Thực hiện chẩn đoán hệ thống trên diện rộng bằng công cụ **AWS X-Ray và CloudWatch Insights**, tinh chỉnh cấu trúc code giúp giảm thiểu đáng kể thời gian khởi động lạnh (Cold Starts) của các hàm Lambda.
* Rà soát toàn bộ các tài khoản và vai trò IAM, thu hẹp quyền hạn về mức tối thiểu cần thiết để đạt các tiêu chuẩn an toàn thông tin khắt khe nhất của doanh nghiệp.

#### 2. Hoàn tất Dự án & Nghiệm thu Xuất sắc
* Tạo lập các ma trận phân tích chi phí trực quan, chứng minh tính hiệu quả vượt trội về mặt kinh tế của hạ tầng Serverless (chỉ trả tiền khi có request) so với mô hình thuê server truyền thống chạy 24/7.
* Thuyết trình thành công toàn bộ hệ sinh thái ứng dụng **AWS BILLO** trước Hội đồng Công nghệ của công ty, nhận được đánh giá rất cao về độ sạch của mã nguồn, tư duy thiết kế hệ thống và khả năng áp dụng nhuần nhuyễn các dịch vụ serverless của AWS.