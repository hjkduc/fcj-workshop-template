---
title: "Sự kiện 1: AWS FIRST CLOUD AI JOURNEY COMMUNITY DAY"
date: 2026-07-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

### Tổng quan sự kiện
* **Tên sự kiện:** AWS FIRST CLOUD AI JOURNEY COMMUNITY DAY
* **Thời gian:** 09:00, Ngày 23/05/2026
* **Địa điểm:** Tầng 26, Tháp Bitexco, 02 Hải Triều, Phường Sài Gòn, Thành phố Hồ Chí Minh
* **Vai trò:** Người tham dự (Attendee)
* **Diễn giả:** Tinh Truong, Anh Pham, Thinh Nguyen, Mai Nguyen, Uyen Le, Thao Nguyen, Duc Dao, Vy Lam

### Các Chủ Đề Cốt Lõi & Kiến Thức Thu Nhận

**1. Bảo mật Hạ tầng & Tối ưu hóa tại Biên (Edge)**
Thinh Nguyen đã mang đến góc nhìn mới về Amazon CloudFront, nhấn mạnh đây là một vành đai bảo mật toàn diện chứ không chỉ là mạng phân phối nội dung (CDN). Việc áp dụng Chính sách giá cố định (Flat-rate Pricing) giúp loại bỏ rủi ro tài chính khi bị tấn công DDoS. Các điểm nhấn kỹ thuật bao gồm Origin Cloaking (ẩn hạ tầng gốc qua VPC Origin) và khả năng chặn đứng các mối đe dọa ngay tại biên mạng.

**2. Bản chất của Tương tác AI & Cơ chế LLM**
Hai bài trình bày đã làm thay đổi tư duy khi làm việc với các Mô hình ngôn ngữ lớn (LLM):
*   **Kỹ thuật Ngữ cảnh:** Tinh Truong khẳng định kết quả AI kém là do ngữ cảnh đầu vào không đạt chuẩn. Việc áp dụng một bộ khung nguyên tắc (Mục tiêu + Thông tin + Ràng buộc + Tiêu chí thành công) là bắt buộc khi đưa AI vào vận hành thực tế.
*   **Lầm tưởng về tính Tất định:** Duc Dao chứng minh rằng việc đặt Temperature = 0 không đảm bảo kết quả giống nhau 100% do sai số dấu phẩy động của GPU và cơ chế gộp batch của API. Thay vào đó, thiết kế hệ thống có khả năng chịu lỗi và sử dụng Temp=0.1 là giải pháp an toàn hơn.

**3. Hệ thống Đa tác nhân (Multi-Agent) & Tự động hóa Dữ liệu**
*   **Ủy ban Tín dụng Ảo:** Vy Lâm trình bày một case-study đột phá về việc chấm điểm tín dụng startup bằng hệ thống Multi-Agent trên Amazon Bedrock. Bằng cách phân chia các tác nhân chuyên biệt (Chuyên viên Tài chính, Phân tích rủi ro...) hoạt động trong môi trường VPC hoàn toàn cô lập, thời gian xử lý hồ sơ đã giảm tới 95%.
*   **Phân tích Data Không cần Code:** Anh Pham demo sức mạnh của Amazon QuickSight Q, cho thấy cách AI tác nhân có thể trực tiếp biến dữ liệu thô thành các quy trình tự động và báo cáo trực quan chỉ bằng ngôn ngữ tự nhiên.

**4. Phát triển Sản phẩm Nhanh (Rapid Prototyping)**
Nhóm LotusHacks (Mai, Uyên, Thảo) chia sẻ hành trình 36 giờ xây dựng công cụ UTMorpho. Dự án minh chứng rằng những sản phẩm tốt nhất luôn khởi nguồn từ những "nỗi đau" thực tế, đồng thời cho thấy kỹ thuật smart-diffing có thể tối ưu hóa đáng kể lượng token tiêu thụ khi AI sinh mã UI.

### Cảm nhận cá nhân
Sự kiện đã kết nối hoàn hảo giữa lý thuyết AI và khả năng triển khai thực tế trên môi trường doanh nghiệp. Các kiến thức chuyên sâu về việc bảo mật hệ thống AI thông qua cơ chế cô lập VPC và tận dụng sức mạnh bảo vệ tại biên của CloudFront cực kỳ hữu ích cho việc thiết kế kiến trúc hạ tầng sau này. Sự kiện củng cố một thực tế: triển khai AI không chỉ nằm ở việc gọi mô hình, mà còn phụ thuộc rất lớn vào hạ tầng mạng an toàn, bảo mật dữ liệu và quản trị ngữ cảnh chặt chẽ.

### Hình ảnh Sự kiện

![Hình ảnh sự kiện](/images/Event1-1.png)
![Hình ảnh sự kiện](/images/Event1-2.png)