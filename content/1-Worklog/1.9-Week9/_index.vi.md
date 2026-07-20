---
title: "Nhật ký Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu Tuần 9:
* Bảo mật tuyệt đối các thông tin nhạy cảm và API Key của mô hình AI đối tác bằng dịch vụ AWS Secrets Manager.
* Thiết lập cơ chế giới hạn tần suất truy cập (Rate Limiting), kiểm soát lưu lượng (Throttling) và gói sử dụng (Usage Plans) trên API Gateway để chống spam.
* Thực hiện rà soát mã nguồn (Code Review) giữa các nhóm và tiến hành đánh giá toàn diện các chính sách an toàn thông tin hệ thống.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Rà soát Mã nguồn & Tiêu chuẩn Lập trình An toàn (Backend & AI)**<br>- **Kiến thức:**<br>  + Nguyên lý Kiểm thử An ninh Ứng dụng Tĩnh (SAST) và Hướng dẫn Lập trình An toàn OWASP.<br>  + Nhận diện rủi ro lộ mã khóa (hardcoded credentials) và lỗi truy cập tài nguyên không hợp lệ (IDOR).<br>  + Kỹ thuật xử lý ngoại lệ (Error handling) ngăn chặn rò rỉ chi tiết nhật ký hệ thống ra màn hình người dùng.<br>- **Thực hành:**<br>  + Thực hiện chéo việc kiểm tra mã nguồn (Code Review) giữa nhóm Backend và nhóm xử lý AI.<br>  + Tái cấu trúc mã nguồn Lambda để loại bỏ hoàn toàn việc lưu mật khẩu trong biến môi trường cục bộ. | 15/06/2026 | 15/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Quản lý & Mã hóa Mật khẩu Tự động với AWS Secrets Manager**<br>- **Kiến thức:**<br>  + Kiến trúc AWS Secrets Manager, chiến lược xoay vòng mật khẩu (secret rotation) và mã hóa KMS.<br>  + Truy vấn mật khẩu động từ AWS SDK vs Kỹ thuật lưu tạm (caching) trong bộ nhớ toàn cục của Lambda.<br>  + Chính sách phân quyền theo tài nguyên (Resource-based policies) bảo vệ chuỗi mật khẩu.<br>- **Thực hành:**<br>  + Khởi tạo chuỗi bí mật trên AWS Secrets Manager lưu trữ API Key của dịch vụ AI bên ngoài.<br>  + Viết mã nguồn cho AWS Lambda (AI Processor) truy vấn động API Key an toàn qua AWS SDK. | 16/06/2026 | 16/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Quản lý Gói Sử dụng (Usage Plans), API Keys & Phân cấp Truy cập API**<br>- **Kiến thức:**<br>  + Cơ chế quản lý Usage Plans, API Keys và kiểm soát hạn mức truy cập của Amazon API Gateway.<br>  + Ánh xạ hạn mức lượt gọi API theo gói dịch vụ Wakan (Free, Plus, Pro) cho tính năng tạo lịch trình.<br>  + Mô hình kiểm tra định dạng Request (Request Validation) chặn dữ liệu rác trước khi gọi Lambda.<br>- **Thực hành:**<br>  + Khởi tạo Usage Plans và API Keys trên API Gateway tương ứng với các phân cấp tài khoản Wakan.<br>  + Tích hợp xác thực token Cognito với API Key và cấu hình quy tắc kiểm tra JSON Schema Request. | 17/06/2026 | 17/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Giới hạn Tần suất Truy cập (Rate Limiting), Throttling & Ngăn chặn Spam**<br>- **Kiến thức:**<br>  + Thuật toán Token Bucket sử dụng trong cơ chế Throttling của Amazon API Gateway.<br>  + Tần suất ổn định (Rate Limit - req/sec) vs Tần suất bùng nổ tối đa (Burst Limit).<br>  + Phương pháp xử lý lỗi HTTP 429 (Too Many Requests) mượt mà phía ứng dụng Client.<br>- **Thực hành:**<br>  + Cấu hình Rate Limiting (50 req/sec) và Burst Limit (100 req/sec) cho các Stage trên API Gateway.<br>  + Giả lập truy cập tải cao để kiểm thử tính chịu tải và xác nhận hệ thống trả về mã lỗi HTTP 429 chuẩn xác. | 18/06/2026 | 18/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Đánh giá Toàn diện Chính sách Bảo mật & Kiến trúc Đám mây**<br>- **Kiến thức:**<br>  + Quy trình kiểm toán an toàn thông tin đám mây, phân tích quyền hạn IAM và an ninh mạng.<br>  + Rà soát tính năng S3 Block Public Access, nhật ký audit CloudWatch và VPC Endpoint Security.<br>- **Thực hành:**<br>  + Thực hiện kiểm toán bảo mật toàn diện trên toàn bộ hạ tầng Wakan (IAM, WAF, API Gateway, S3, Secrets Manager).<br>  + Lập báo cáo kiểm toán nội bộ và thu hồi các quyền hạn thừa phát sinh trong quá trình phát triển. | 19/06/2026 | 19/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 9:

#### Thứ Hai (15/06/2026):
* Hoàn tất đợt rà soát mã nguồn (Code Review) giữa nhóm Backend và AI, đảm bảo tuân thủ nghiêm ngặt các tiêu chuẩn lập trình an toàn OWASP.
* Tái cấu trúc toàn bộ các hàm Lambda backend, loại bỏ hoàn toàn các giá trị cấu hình nhạy cảm và ngăn chặn việc rò rỉ chi tiết hệ thống khi xảy ra ngoại lệ.
* Chuẩn hóa cấu trúc dữ liệu phản hồi lỗi định dạng JSON, giúp giao diện người dùng hiển thị thông báo thân thiện và chính xác.

#### Thứ Ba (16/06/2026):
* Mã hóa và lưu trữ cô lập toàn bộ API Key kết nối mô hình AI đối tác vào dịch vụ AWS Secrets Manager sử dụng khóa mã hóa KMS.
* Lập trình tính năng lấy mật khẩu động trong hàm AWS Lambda (AI Processor) thông qua AWS SDK, kết hợp lưu đệm biến toàn cục để tối ưu độ trễ và chi phí gọi API.
* Thiết lập chính sách phân quyền tài nguyên chặt chẽ, chỉ cho phép duy nhất IAM Role của Lambda AI Processor có quyền giải mã và lấy khóa API.

#### Thứ Tư (17/06/2026):
* Thiết lập thành công các gói Usage Plans và API Keys trên Amazon API Gateway tương ứng với hạn mức của các gói dịch vụ Wakan (Free, Plus, Pro).
* Bật tính năng Request Validation trên API Gateway để lọc bỏ các yêu cầu sai định dạng ngay tại biên, tránh lãng phí tài nguyên tính toán của Lambda.
* Kết nối luồng xác thực người dùng Cognito với hệ thống quản lý Usage Plan của API Gateway.

#### Thứ Năm (18/06/2026):
* Cấu hình quy tắc giới hạn tần suất (Rate Limiting) và giới hạn bùng nổ (Burst Throttling) trên API Gateway để ngăn chặn các hành vi cố tình spam hệ thống.
* Bảo vệ an toàn cho các hàm Lambda backend và mô hình AI đối tác khỏi nguy cơ quá tải và phát sinh chi phí ngoài tầm kiểm soát.
* Chạy thử nghiệm giả lập tải cao và xác nhận hệ thống phản hồi chính xác mã lỗi HTTP 429 (Too Many Requests) khi truy cập vượt hạn mức.

#### Thứ Sáu (19/06/2026):
* Hoàn thành kỳ kiểm toán an toàn thông tin nội bộ trên toàn bộ các thành phần hạ tầng đám mây của dự án Wakan.
* Xác nhận tất cả S3 Buckets đều bật tính năng Block Public Access, CloudFront tích hợp OAC, và các IAM Roles tuân thủ nghiêm ngặt Nguyên tắc Đặc quyền Tối thiểu.
* Lập tài liệu báo cáo kết quả kiểm toán bảo mật và chính thức phê duyệt hạ tầng sẵn sàng cho giai đoạn tích hợp giám sát tập trung.