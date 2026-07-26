---
title: "Sự kiện 4"
date: 2026-07-25
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---

# Xây dựng Agentic AI

## Mục Tiêu Sự Kiện

- Giới thiệu cách các team tiếp cận việc xây dựng sản phẩm Agentic AI trong các tình huống thực tế.
- Học cách biến yêu cầu còn mơ hồ thành kiến trúc, workflow và demo có thể trình bày được.
- So sánh 4 hướng dự án khác nhau: tự động hóa kiến trúc giải pháp, đặt món qua hội thoại, prototype hackathon và phân tích tín hiệu doanh nghiệp để hỗ trợ ra quyết định.
- Ghi lại những bài học thực tế về xây dựng, kiểm thử, thuyết trình và cải tiến sản phẩm AI.

---

## Danh Sách Team / Dự Án

- **Plan V** - *Solution Architect Professional Native App*
- **One Team** - *AI-Powered Conversation Ordering*
- **3KA** - *Hackathon Journey / S.H.E.P.H.E.R.D.*
- **Signal Scout** - *Phân tích tín hiệu doanh nghiệp dựa trên bằng chứng*

---

## Những Điểm Nổi Bật

### 1. Từ yêu cầu đến kiến trúc

Nhóm **Solution Architect Professional Native App** cho thấy cách biến yêu cầu viết bằng ngôn ngữ tự nhiên thành một quy trình thiết kế có cấu trúc hơn.

Phần demo tập trung vào việc hỗ trợ solution architect:

- Đọc yêu cầu dự án nhanh hơn.
- Phác thảo kiến trúc ban đầu.
- Tạo sơ đồ có thể chỉnh sửa.
- Đưa ra ước lượng chi phí AWS ở mức định hướng.

Điểm hay nhất là công cụ không thay thế kiến trúc sư. Nó tạo ra một bản nháp có cơ sở để người làm có thể xem lại, chỉnh sửa và hoàn thiện nhanh hơn nhiều so với việc bắt đầu từ trang trắng.

### 2. Hội thoại chính là giao diện sản phẩm

Phần trình bày của **One Team** giới thiệu một agent đặt món qua hội thoại trên các kênh như Zalo và Messenger.

Dự án cho thấy đặt món trong chat không chỉ là bài toán chatbot. Đây là bài toán hệ thống, phải xử lý được:

- Chọn món.
- Cập nhật số lượng.
- Biến thể và luật nghiệp vụ.
- Kiểm tra giỏ hàng.
- Luồng từ ý định ban đầu đến đơn hàng đã xác nhận.

Thông điệp rất rõ: một agent tốt phải thực sự thực hiện nghiệp vụ, chứ không chỉ trả lời cho hay.

### 3. Cảm giác thật sự khi làm hackathon

Nhóm **3KA** chia sẻ hành trình xây dựng **S.H.E.P.H.E.R.D.**, một ý tưởng theo dõi đám đông và cảnh báo rủi ro được làm trong 24 giờ hackathon.

Phần chia sẻ nói về:

- Áp lực khi phải build trong thời gian rất ngắn.
- Cách ý tưởng thay đổi trong quá trình làm.
- Những gì học được từ computer vision thời gian thực và workflow agentic.
- Các thách thức lớn như độ trễ, tracking, phạm vi bài toán và độ tin cậy.

Phần này rất đáng nhớ vì nó cho thấy mặt thật của việc làm sản phẩm: bối rối, mệt, debug, làm việc nhóm, và cảm giác vui khi kịp làm ra thứ chạy được đúng lúc.

### 4. Kết nối các tín hiệu rời rạc thành một câu chuyện rõ ràng

Nhóm **Signal Scout** trình bày một hệ thống AI được thiết kế để phát hiện sớm các thay đổi chiến lược của doanh nghiệp bằng cách thu thập, xác thực và phân tích bằng chứng từ nhiều nguồn khác nhau.

Giá trị mà sản phẩm hướng tới là giúp các nhóm:

- Kết nối các tín hiệu rời rạc thành một bức tranh thống nhất.
- Xây dựng kịch bản từ dữ liệu tài chính và vận hành.
- Hiển thị timeline và cảnh báo rủi ro.
- Hỗ trợ các quyết định kiểu maintain, adapt, hoặc accelerate bằng bằng chứng minh bạch.

Phần kiến trúc và ước lượng chi phí cũng cho thấy nhóm đã nghĩ đến ràng buộc sản phẩm thực tế, chứ không chỉ dừng ở lớp AI.

---

## Những Gì Học Được

### Agentic AI không chỉ là prompt

Sự kiện giúp mình hiểu rõ hơn rằng Agentic AI không chỉ là chuyện viết prompt cho model. Nó phải cần có:

- Workflow rõ ràng.
- Sử dụng công cụ phù hợp.
- Các bước kiểm tra lại kết quả.
- Rào chắn hợp lý cho những hành động ảnh hưởng đến nghiệp vụ thật.

### Demo tốt thường bắt đầu từ phạm vi rõ ràng

Mỗi team có một hướng khác nhau, nhưng điểm chung là đều chọn một ý tưởng đủ sắc nét thay vì ôm quá nhiều thứ cùng lúc.

Điều đó làm demo dễ hiểu hơn và đáng tin hơn.

### Làm theo nhóm dạy nhiều hơn làm một mình

Hành trình hackathon cho thấy làm việc theo nhóm, giới hạn thời gian và áp lực trình bày sẽ làm lộ ra những khoảng trống mà khi tự học thường không thấy.

Nhưng chính ở đó lại có nhiều bài học nhất: kiểm soát phạm vi, phân vai rõ, lặp nhanh, và học cách giải thích sản phẩm một cách đơn giản.

### Dữ liệu và bằng chứng rất quan trọng trong AI hỗ trợ quyết định

Signal Scout bổ sung một bài học rất quan trọng: khi AI được dùng để hỗ trợ ra quyết định trong doanh nghiệp, hệ thống phải minh bạch và có thể kiểm chứng.

Không chỉ cần tạo ra câu trả lời, sản phẩm còn phải có lớp thu thập bằng chứng, quy tắc phân tích và cách giải thích rõ vì sao lại đưa ra khuyến nghị đó.

---

## Cảm Nhận Cá Nhân

Sự kiện này cho mình góc nhìn rộng hơn về Agentic AI trong thực tế.

Mình thích nhất cách mỗi team giải quyết một bài toán khác nhau:

- Biến yêu cầu thành kiến trúc.
- Biến hội thoại thành workflow đặt món.
- Biến một ý tưởng hackathon thành prototype có thể demo được.
- Biến các tín hiệu rời rạc của doanh nghiệp thành công cụ hỗ trợ ra quyết định.

Điều này nhắc mình rằng chất lượng của một sản phẩm AI không chỉ nằm ở model, mà còn nằm ở cách toàn bộ hệ thống được thiết kế, giải thích và trình bày.

---

## Kết Luận

FCAJ Agentic AI Build Week là một buổi recap hữu ích về cách mọi người đang ứng dụng AI theo nhiều hướng sản phẩm khác nhau.

Sự kiện cho mình thêm nhiều ý tưởng thực tế về kiến trúc, thiết kế workflow, phân tích dựa trên bằng chứng và tư duy cải tiến sản phẩm AI thông qua lặp lại và làm việc nhóm.
