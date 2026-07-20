---
title: "Nhật ký Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu Tuần 11:
* Thực hiện kiểm thử xâm nhập (Penetration Testing) cơ bản và giả lập các kịch bản tấn công nhằm xác minh hiệu quả của các biện pháp bảo mật biên và ứng dụng.
* Rà soát toàn bộ các chính sách phân quyền IAM bằng IAM Access Analyzer, triệt tiêu nguy cơ leo thang đặc quyền và rò rỉ dữ liệu nhạy cảm.
* Khắc phục các lỗ hổng phát sinh, gia cố hạ tầng và hoàn thiện Báo cáo Kiểm toán An toàn Thông tin Đám mây trước buổi Demo sản phẩm.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Rà soát Kết quả Kiểm thử & Thống nhất Tiêu chí Bảo mật**<br>- **Kiến thức:**<br>  + Phương pháp kiểm thử xâm nhập (Penetration Testing) cho kiến trúc Serverless, thang đo mức độ lỗ hổng CVSS v3.1, OWASP Top 10 API Security Risks.<br>  + Thiết lập phạm vi đánh giá an toàn thông tin trên các tầng Frontend, API và Database.<br>- **Thực hành:**<br>  + Phân tích kết quả kiểm thử E2E cùng các nhóm, xác định phạm vi kiểm thử an ninh và cấu hình các công cụ giả lập tấn công (OWASP ZAP, Postman). | 29/06/2026 | 29/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Kiểm thử Xâm nhập & Giả lập Tấn công qua WAF (SQLi, XSS, Rate Limits)**<br>- **Kiến thức:**<br>  + Các kỹ thuật khai thác lỗ hổng Web (SQL Injection, Cross-Site Scripting - XSS, Parameter Tampering, HTTP Flood).<br>  + Cơ chế đánh giá quy tắc của AWS WAF và phân tích nhật ký truy cập bị chặn (Sampled Logs).<br>- **Thực hành:**<br>  + Sử dụng OWASP ZAP bắn các chuỗi payload độc hại thử nghiệm vào các cổng CloudFront và API Gateway.<br>  + Kiểm tra khả năng chặn tấn công của AWS WAF và rà soát log bị chặn trên CloudWatch. | 30/06/2026 | 30/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Gia cố Chính sách IAM & Kiểm toán Đặc quyền Tối thiểu**<br>- **Kiến thức:**<br>  + Tự động hóa kiểm toán IAM bằng công cụ AWS IAM Access Analyzer.<br>  + Nhận diện các nguy cơ leo thang đặc quyền và rủi ro từ việc lạm dụng ký tự đại diện (`*`) trong chính sách IAM.<br>  + Áp dụng các từ khóa điều kiện bắt buộc (`aws:PrincipalTag`, `aws:SecureTransport`).<br>- **Thực hành:**<br>  + Quét toàn bộ Lambda execution roles và IAM policies bằng IAM Access Analyzer.<br>  + Giới hạn các quyền đại diện (`*`) về chính xác ARN của bảng DynamoDB/S3 bucket và thu hồi các quyền hạn thừa. | 01/07/2026 | 01/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Kiểm toán Secrets Manager, Chống Rò rỉ Dữ liệu & Kiểm tra Mã hóa**<br>- **Kiến thức:**<br>  + Ngăn chặn rò rỉ dữ liệu (DLP) trên môi trường Cloud, chính sách khóa KMS, nhật ký xoay vòng mật khẩu.<br>  + Nhận diện nguy cơ lộ chuỗi mật khẩu trong luồng log CloudWatch hoặc dữ liệu phản hồi API.<br>- **Thực hành:**<br>  + Kiểm toán nhật ký truy cập AWS Secrets Manager và dùng CloudWatch Logs Insights kiểm tra đảm bảo không có API Key bị ghi log thô.<br>  + Cấu hình KMS Key Policy chặt chẽ, chỉ cho phép các IAM Role được chỉ định mới có quyền giải mã. | 02/07/2026 | 02/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Khắc phục Lỗ hổng, Gia cố Hạ tầng & Lập Báo cáo Bảo mật Tóm tắt**<br>- **Kiến thức:**<br>  + Chiến lược khắc phục sai lệch cấu hình an ninh mạng, gia cố chính sách CORS và kiểm tra định dạng Request.<br>  + Soạn thảo Báo cáo Đánh giá An toàn Thông tin Đám mây (Cloud Security Assessment Report) chuẩn doanh nghiệp.<br>- **Thực hành:**<br>  + Sửa đổi các lỗ hổng nhỏ phát hiện được (thắt chặt CORS origin, cấu hình chặt chẽ Request Model trên API Gateway).<br>  + Tổng hợp dữ liệu kiểm toán và lập Báo cáo Kiểm toán An toàn Thông tin hoàn chỉnh cho Wakan. | 03/07/2026 | 03/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 11:

#### Thứ Hai (29/06/2026):
* Tổ chức họp nhóm đánh giá kết quả kiểm thử toàn hệ thống và chốt phạm vi thực hiện kiểm thử xâm nhập (Penetration Testing) cho Wakan.
* Khởi tạo và cấu hình bộ công cụ quét lỗ hổng an ninh mạng (OWASP ZAP, Burp Suite, Postman).
* Thống nhất tiêu chí đánh giá mức độ nghiêm trọng của lỗ hổng dựa trên chuẩn CVSS v3.1 và danh mục OWASP Top 10 API Security.

#### Thứ Ba (30/06/2026):
* Thực hiện giả lập các cuộc tấn công mạng thực tế (SQL Injection, XSS, HTTP Flood) hướng vào các cổng giao tiếp của Wakan.
* Xác minh hệ thống tường lửa AWS WAF Web ACLs hoạt động chính xác, đánh chặn và ngăn chặn thành công 100% các yêu cầu chứa mã độc tại biên mạng.
* Kiểm tra nhật ký WAF Sampled Logs trên CloudWatch để xác nhận các quy tắc chặn IP và quy tắc bảo mật hoạt động đúng thiết kế.

#### Thứ Tư (01/07/2026):
* Thực hiện kiểm toán toàn bộ các chính sách phân quyền IAM của các hàm Lambda bằng AWS IAM Access Analyzer.
* Loại bỏ hoàn toàn các quyền đại diện quá rộng (`*`), giới hạn chính xác phạm vi truy cập vào các ARN bảng DynamoDB của Wakan.
* Đảm bảo tất cả các IAM Execution Role đều tuân thủ nghiêm ngặt Nguyên tắc Đặc quyền Tối thiểu (Principle of Least Privilege).

#### Thứ Năm (02/07/2026):
* Rà soát nhật ký truy cập dịch vụ AWS Secrets Manager và chính sách khóa KMS bảo vệ API Key của mô hình AI đối tác.
* Thực hiện truy vấn trên CloudWatch Logs Insights kiểm tra toàn bộ luồng log, xác nhận không có bất kỳ chuỗi mật khẩu hay API Key thô nào bị rò rỉ out-log.
* Giới hạn quyền giải mã KMS strictly chỉ gán cho duy nhất IAM Execution Role của hàm AWS Lambda (AI Processor).

#### Thứ Sáu (03/07/2026):
* Khắc phục triệt để các cấu hình an toàn mạng nhỏ, thắt chặt quy tắc CORS Origin trên API Gateway chỉ cho phép tên miền chính thức của Wakan truy cập.
* Kiểm tra tính năng JSON Schema Validation trên API Gateway, đảm bảo lọc bỏ các Request sai cấu trúc trước khi chuyển tới tầng tính toán.
* Tổng hợp toàn bộ kết quả thực nghiệm bảo mật và hoàn thiện Báo cáo Kiểm toán An toàn Thông tin Đám mây cho nền tảng Wakan.