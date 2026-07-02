---
title: "Sự kiện 2"
date: 2026-06-06
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

## Mục đích của sự kiện

- Giới thiệu tầm quan trọng của Prompt Engineering trong việc tối ưu chất lượng đầu ra của các mô hình ngôn ngữ lớn.
- Cung cấp một khung chuẩn và các thành phần cốt lõi để xây dựng prompt hiệu quả.
- Chia sẻ các phương pháp prompting nâng cao và chiến lược tối ưu chi phí token khi sử dụng AI.
- Demo kiến trúc AWS serverless thực tế thông qua ứng dụng **Proptimizer**.

---

## Danh sách diễn giả

- **Bao Huynh** - Junior Cloud Native Developer, Endava Vietnam
- **Le Hoang Gia Dai**
- **Nguyen Quoc Bao**
- **Truong Huy Phuoc**
- **Viet Phat** - AI Majoring at Swinburne University of Technology
- **Tran Trung Vinh** - System Administrator at Central Retail Group

---

## Nội dung nổi bật

### 1. Tư duy cốt lõi của Prompt Engineering

Prompt Engineering không chỉ là việc nhập câu hỏi cho AI. Đây là quá trình cấu trúc cách người dùng giao tiếp với mô hình AI để mô hình hiểu rõ nhiệm vụ, ngữ cảnh, ràng buộc và định dạng đầu ra mong muốn.

Nếu không có prompt rõ ràng, người dùng có thể gặp nhiều vấn đề:

- **Prompt chung chung** dẫn đến phản hồi mơ hồ và ít giá trị.
- **Lãng phí token** làm tăng chi phí vận hành.
- **Hướng dẫn không rõ ràng** tạo ra kết quả thiếu nhất quán.
- **Giao tiếp kém với AI** làm giảm năng suất và tốn thời gian chỉnh sửa.

---

### 2. Cấu trúc của một prompt hiệu quả

Để cải thiện chất lượng đầu ra của LLM, một prompt nên có bảy thành phần cơ bản:

- **Role**: Xác định vai trò hoặc góc nhìn chuyên môn mà mô hình cần đảm nhận.
- **Instruction**: Nêu rõ nhiệm vụ cụ thể mà mô hình cần thực hiện.
- **Context**: Cung cấp thông tin nền và giới hạn tình huống.
- **Input Data**: Cung cấp dữ liệu hoặc nội dung cần xử lý.
- **Output Format**: Xác định cấu trúc kết quả mong muốn, ví dụ JSON, Markdown, bảng hoặc tóm tắt.
- **Examples**: Cung cấp ví dụ mẫu để mô hình noi theo.
- **Constraints/Guidelines**: Đặt ra ràng buộc, giọng văn, giới hạn và những điều cần tránh.

---

### 3. Các phương pháp prompting nâng cao

Sự kiện giới thiệu một số kỹ thuật prompting nâng cao:

- **Chain-of-Thought (CoT)**: Hướng dẫn mô hình suy luận từng bước trước khi đưa ra câu trả lời cuối cùng.
- **Self-Consistency**: Chạy nhiều hướng suy luận và chọn kết quả nhất quán nhất.
- **Tree-of-Thoughts (ToT)**: Cho phép mô hình khám phá nhiều nhánh suy luận và đánh giá các hướng giải quyết khác nhau.
- **RAG (Retrieval-Augmented Generation)**: Kết hợp truy xuất thông tin bên ngoài với khả năng sinh văn bản của LLM.
- **Role Prompting**: Gán vai trò cụ thể để kiểm soát giọng văn, từ vựng và phong cách phản hồi.

---

### 4. Hiểu về Token Economics

Sự kiện cũng giải thích tầm quan trọng của token economics khi sử dụng mô hình AI.

Các ý chính gồm:

- LLM xử lý văn bản bằng token, thường là các phần nhỏ của từ thay vì toàn bộ từ.
- Mức tiêu thụ token có thể khác nhau giữa các ngôn ngữ.
- Tiếng Việt có thể tốn nhiều token hơn tiếng Anh cho cùng một ý nghĩa.
- Viết prompt ngắn gọn và có cấu trúc giúp giảm chi phí.
- Chi phí token cần được cân nhắc trước khi tích hợp AI vào hệ thống production.

---

### 5. Triển khai thực tế: Kiến trúc Proptimizer

Các diễn giả đã giới thiệu **Proptimizer**, một browser extension giúp tự động hóa Prompt Engineering và hỗ trợ tương tác với AI trực tiếp trên bất kỳ trang web nào.

Ứng dụng được xây dựng trên kiến trúc serverless của AWS, bao gồm:

- **CloudFront và Amazon S3** để phân phối frontend.
- **Amazon Cognito** để xác thực người dùng.
- **Amazon API Gateway** để định tuyến request backend.
- **AWS Lambda** để xử lý logic backend serverless.
- **Amazon Bedrock** để tích hợp mô hình AI.
- **Amazon DynamoDB** để lưu trữ dữ liệu.
- **Amazon CloudWatch** để ghi log và giám sát hệ thống.

Kiến trúc này cho thấy một ứng dụng AI có thể được thiết kế với chi phí hạ tầng thấp nhưng vẫn đảm bảo khả năng mở rộng và dễ bảo trì.

---

## Bài học và cảm nhận cá nhân

### Thay đổi cách tương tác với AI

Sự kiện này giúp tôi thay đổi cách nhìn về Prompt Engineering. Tôi học được rằng chất lượng đầu ra của AI phụ thuộc rất nhiều vào độ rõ ràng của dữ liệu đầu vào. Thay vì viết các prompt ngắn và thiếu ngữ cảnh, tôi nên cung cấp rõ vai trò, bối cảnh, ràng buộc và định dạng kết quả mong muốn.

Cách làm này giúp tiết kiệm thời gian vì giảm số lần phải chỉnh sửa hoặc hỏi lại AI do kết quả chưa đúng.

### Góc nhìn thực tế về Cloud và Serverless

Điểm nổi bật của sự kiện là việc một kiến trúc cloud lý thuyết được triển khai thành một browser extension AI thực tế.

Proptimizer cho thấy các dịch vụ serverless của AWS có thể hỗ trợ xây dựng một sản phẩm AI thực tế. Sự kết hợp giữa CloudFront, S3, API Gateway, Lambda, Bedrock, DynamoDB, Cognito và CloudWatch là một kiến trúc tham khảo hữu ích cho các ứng dụng AI trong tương lai.

---

## Kế hoạch ứng dụng vào công việc

Sau sự kiện này, tôi có thể áp dụng kiến thức vào các công việc sau:

- **Sử dụng prompt template có cấu trúc** cho lập trình, debug và viết tài liệu kỹ thuật.
- **Áp dụng Chain-of-Thought prompting** cho các bài toán phân tích phức tạp.
- **Ước lượng token usage và chi phí** trước khi sử dụng AI trong môi trường production.
- **Áp dụng mô hình serverless architecture** như CloudFront + S3 + API Gateway + Lambda cho các ứng dụng tương lai.
- **Tham khảo kiến trúc Proptimizer** khi thiết kế ứng dụng AI trên AWS.
- **Cải thiện teamwork với AI** bằng cách dùng prompt format thống nhất giữa các thành viên.

---

## Kết luận

Sự kiện ngày 06/06 mang lại kiến thức hữu ích ở hai khía cạnh: Prompt Engineering nâng cao và thiết kế ứng dụng serverless hiện đại trên AWS.

Sự kiện giúp tôi hiểu cách giao tiếp với AI hiệu quả hơn và cách thiết kế các hệ thống AI-powered bằng các dịch vụ AWS tối ưu chi phí.
