---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:
- Nghiên cứu các công cụ tự động hóa hạ tầng dưới dạng mã nguồn: AWS CloudFormation và AWS SAM (Serverless Application Model).
- Hiểu rõ lợi ích của Hạ tầng dưới dạng mã (Infrastructure as Code - IaC) so với việc cấu hình thủ công bằng click chuột trên trình duyệt.
- Tự tay viết các template cơ sở định nghĩa các tham số serverless căn bản.
- Xây dựng một quy trình deploy đồng bộ được điều khiển hoàn toàn bằng mã nguồn tại local.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| :--- | :--- | :--- | :--- | :--- |
| 2 | - Làm việc trực tiếp tại văn phòng công ty <br> - Thống nhất các tiêu chuẩn phát triển xoay quanh AWS SAM để phục vụ cấu hình nhanh, kiểm thử local và triển khai có cấu trúc | 25/05/2026 | 25/05/2026 | Văn phòng công ty |
| 3 | - Học giải phẫu cấu trúc của một file template AWS SAM: globals, resources, outputs và các phạm vi biến đổi (Transform) <br> - Cài đặt bộ công cụ AWS SAM CLI trên hệ thống máy tính phát triển | 26/05/2026 | 26/05/2026 | https://cloudjourney.awsstudygroup.com/ |
| 4 | - Xây dựng một file `template.yaml` cơ bản định nghĩa môi trường chạy cho một hàm AWS Lambda cô lập <br> - Thực hiện giả lập chạy thử hàm local sử dụng các lớp container được ảo hóa qua công cụ Docker | 27/05/2026 | 27/05/2026 | https://cloudjourney.awsstudygroup.com/ |
| 5 | - Mở rộng cấu trúc tệp tin SAM để khai báo thêm một khối tài nguyên Amazon DynamoDB tích hợp <br> - Thực hành các cơ chế deploy lên cloud thông qua các câu lệnh `sam build` và `sam deploy --guided` | 28/05/2026 | 28/05/2026 | https://cloudjourney.awsstudygroup.com/ |
| 6 | - Gỡ lỗi (Debug) các vấn đề về quyền thực thi cloud ban đầu, hiện tượng lệch template (Drift) và ánh xạ vai trò IAM <br> - Chuẩn hóa các tham số chạy môi trường (Environment Parameters) qua các cấu hình phân tách biệt | 29/05/2026 | 29/05/2026 | https://cloudjourney.awsstudygroup.com/ |

---

### Kết quả đạt được tuần 6:

#### 1. Áp dụng hạ tầng dưới dạng mã (IaC)
* Chuyển dịch thành công tư duy quản lý hạ tầng đám mây sang **Hạ tầng dưới dạng mã (IaC)** với **AWS SAM**, đảm bảo mọi tài nguyên phân bổ trên môi trường dev đều có tính nhất quán và có khả năng tái tạo.
* Cài đặt, cấu hình và kiểm thử thành công bộ công cụ AWS SAM CLI kết hợp với môi trường Docker để giả lập chính xác runtime của đám mây ngay dưới local.

#### 2. Khai báo tài nguyên dạng mã nguồn (Declarative)
* Tự tay viết các file YAML sạch sẽ, điều khiển bằng tham số giúp triển khai các module serverless đồng bộ.
* Thực hiện thành công các lượt deploy có hướng dẫn lên hệ thống đám mây, theo dõi và quản lý chặt chẽ vòng đời của CloudFormation Stack cũng như cơ chế tự động Rollback khi xảy ra lỗi trực tiếp từ cửa sổ Terminal.