---
title: "Sự kiện 1"
date: 2026-05-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

## Mục đích của sự kiện

- Giới thiệu tầm quan trọng của Prompt Engineering trong việc nâng cao chất lượng đầu ra của các mô hình ngôn ngữ lớn.
- Hướng dẫn cách xây dựng một prompt hiệu quả với đầy đủ các thành phần cần thiết.
- Giới thiệu các kỹ thuật prompting nâng cao và cách tối ưu chi phí khi sử dụng AI.
- Demo sản phẩm thực tế **Proptimizer** – browser extension tự động tối ưu hóa prompt.

---

## Danh sách diễn giả

- **Huỳnh Hoàng Long** - Admin of FCAJ
- **Nguyễn Tuấn Thịnh** - DevOps/Cloud Engineer, First Cloud AI Journey
- **Khang Nguyen** - Solution Architect
- **Nguyễn Phương Thảo** - Application Cloud Dev

---

## Nội dung nổi bật

### Automated Prompt Engineering: Enhancing LLM Output Quality

Bài trình bày của diễn giả **Nguyễn Tuấn Thịnh** tập trung vào việc viết prompt đúng cách để khai thác tối đa khả năng của các mô hình AI, đồng thời giới thiệu sản phẩm Proptimizer được xây dựng trên nền tảng AWS.

### Vấn đề khi không biết viết prompt tốt

- Prompt chung chung dẫn đến output chung chung, ít giá trị.
- Lãng phí token làm tăng chi phí vận hành.
- Hướng dẫn mơ hồ khiến kết quả không nhất quán.
- Giao tiếp kém với AI làm giảm năng suất.

### Bảy thành phần của một prompt hiệu quả

- **Role**: Xác định vai trò mô hình cần đóng, ví dụ career coach hoặc senior developer.
- **Instruction**: Nhiệm vụ cụ thể mô hình cần thực hiện.
- **Context**: Thông tin nền liên quan đến bài toán.
- **Input Data**: Dữ liệu đầu vào cần xử lý.
- **Output Format**: Định dạng hoặc cấu trúc kết quả mong muốn.
- **Examples**: Ví dụ mẫu để mô hình noi theo.
- **Constraints/Guidelines**: Ràng buộc như giới hạn từ, phong cách viết hoặc điều không được làm.

### Nguyên tắc viết prompt tốt

- Viết rõ ràng và cụ thể.
- Sử dụng ngôn ngữ chỉ thị.
- Dùng delimiter để phân tách các phần của prompt.
- Mô tả những gì cần làm, không chỉ nêu những điều không được làm.
- Không yêu cầu LLM tính toán số học chính xác.
- Cho phép mô hình trả lời “Tôi không biết” thay vì bịa đặt.
- Chia nhỏ input dài thành các phần nhỏ hơn.

### Kỹ thuật prompting nâng cao

- **Chain-of-Thought (CoT)**: Yêu cầu mô hình suy nghĩ từng bước trước khi trả lời.
- **Self-Consistency**: Chạy nhiều hướng suy luận và chọn câu trả lời nhất quán nhất.
- **Tree-of-Thoughts (ToT)**: Khám phá nhiều nhánh suy luận song song.
- **RAG (Retrieval-Augmented Generation)**: Kết hợp tìm kiếm dữ liệu ngoài với khả năng sinh văn bản.
- **Role Prompting**: Gán vai trò cụ thể để định hướng phong cách trả lời.

### Token Economics

- Token là đơn vị xử lý của LLM.
- Token không hoàn toàn giống từ mà có thể là các phần nhỏ của từ.
- Số lượng token khác nhau giữa các ngôn ngữ, trong đó tiếng Việt thường tốn nhiều token hơn tiếng Anh cho cùng một ý nghĩa.
- Prompt ngắn gọn và chính xác giúp giảm chi phí vận hành AI.

### Sản phẩm Proptimizer

Proptimizer là một browser extension có khả năng tự động tối ưu hóa prompt của người dùng và cho phép chat với AI trực tiếp trên bất kỳ trang web nào.

Kiến trúc của Proptimizer sử dụng các dịch vụ AWS như CloudFront và S3 cho frontend, Cognito cho xác thực, API Gateway và Lambda cho backend serverless, Amazon Bedrock cho AI engine, DynamoDB để lưu trữ dữ liệu và CloudWatch để monitoring.

---

## Những gì học được

### Tư duy khi làm việc với AI

- Prompt là giao tiếp, không chỉ là câu lệnh.
- Context quyết định rất lớn đến chất lượng output.
- Prompt ngắn gọn, đúng trọng tâm có thể vừa giảm chi phí vừa cải thiện độ chính xác.

### Kỹ thuật thực tế

- Biết cách áp dụng bảy thành phần của prompt vào các tình huống thực tế.
- Hiểu sự khác biệt giữa CoT, Self-Consistency và ToT để chọn kỹ thuật phù hợp.
- Nhận ra rằng LLM không phù hợp cho tính toán số học chính xác và nên kết hợp với công cụ chuyên dụng.

### Kiến trúc serverless thực tế

- Hiểu cách một sản phẩm AI thực tế có thể được xây dựng trên AWS serverless.
- Hiểu luồng: User → CloudFront → API Gateway → Lambda → Bedrock → DynamoDB.
- Nhận ra rằng có thể xây dựng ứng dụng AI với chi phí hạ tầng thấp nếu tận dụng đúng các dịch vụ managed của AWS.

---

## Ứng dụng vào công việc

- Áp dụng bảy thành phần prompt vào các tác vụ hằng ngày như viết code, debug và viết tài liệu.
- Thử nghiệm Chain-of-Thought prompting cho các bài toán phân tích yêu cầu suy luận từng bước.
- Tính toán token cost trước khi đưa AI vào production.
- Tham khảo kiến trúc Proptimizer để thiết kế các ứng dụng AI serverless.
- Thực hành viết prompt có cấu trúc khi làm việc nhóm để đảm bảo output nhất quán.

---

## Trải nghiệm trong event

Tham gia sự kiện của **First Cloud AI Journey** ngày 09/05 là một trải nghiệm thực tế và gần gũi, đặc biệt phù hợp với những người đang sử dụng AI hằng ngày nhưng chưa biết cách khai thác AI đúng cách.

### Góc nhìn mới về Prompt Engineering

Trước đây tôi thường nhập prompt ngắn gọn và chấp nhận kết quả trả về. Sau buổi này, tôi hiểu rằng chất lượng output phụ thuộc trực tiếp vào chất lượng input. Một prompt có đủ role, context và constraints sẽ cho kết quả tốt hơn nhiều so với một câu hỏi chung chung.

### Ấn tượng với sản phẩm Proptimizer

Nhóm tác giả không chỉ dừng ở lý thuyết mà đã hiện thực hóa thành một browser extension hoàn chỉnh. Sản phẩm cũng cho thấy cách các dịch vụ serverless của AWS có thể hỗ trợ một ứng dụng AI thực tế với chi phí hạ tầng thấp.

### Bài học rút ra

- Prompt Engineering là kỹ năng giao tiếp thực tế có thể học và luyện tập.
- Hiểu token economics giúp đưa ra quyết định kỹ thuật và tài chính tốt hơn khi tích hợp AI vào sản phẩm.
- Kiến trúc serverless kết hợp với managed AI services như Amazon Bedrock là hướng đi thực tế để xây dựng sản phẩm AI.

---

## Kết luận

Tổng thể, buổi event không chỉ cung cấp kiến thức lý thuyết mà còn cho thấy cách áp dụng thực tế qua sản phẩm Proptimizer. Sự kiện giúp tôi thay đổi cách tiếp cận khi làm việc với AI và có thêm định hướng rõ ràng hơn để xây dựng ứng dụng AI trên nền tảng AWS.
