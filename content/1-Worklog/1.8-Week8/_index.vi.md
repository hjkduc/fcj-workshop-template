---
title: "Nhật ký Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu Tuần 8:
* Thống nhất tài liệu chuẩn hóa API Contract giữa các nhóm Frontend, Backend và AI Processor.
* Triển khai hạ tầng lưu trữ và phân phối giao diện ứng dụng Wakan sử dụng Amazon S3 kết hợp Amazon CloudFront bảo mật qua Origin Access Control (OAC).
* Xây dựng vành đai bảo mật biên với AWS WAF, cấu hình quản lý định danh qua Amazon Cognito User Pools và phân quyền đặc quyền tối thiểu cho AWS Lambda.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Đồng bộ API Contract & Định nghĩa Schema (Frontend-Backend-AI)**<br>- **Kiến thức:**<br>  + Chuẩn thiết kế RESTful API, tài liệu cấu trúc OpenAPI (Swagger) 3.0, kiểm tra JSON Schema.<br>  + Cấu trúc giao tiếp bất đồng bộ giữa các tầng ứng dụng cho tác vụ sinh lịch trình du lịch AI.<br>- **Thực hành:**<br>  + Viết bản thảo OpenAPI spec cho các cổng API dự án Wakan (`/itinerary`, `/preferences`, `/user/profile`).<br>  + Thống nhất thông số Request/Response và các mã lỗi tiêu chuẩn giữa 3 nhóm Frontend, Backend và AI. | 08/06/2026 | 08/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Phân phối Giao diện qua Amazon S3 & Tăng tốc CDN với CloudFront**<br>- **Kiến thức:**<br>  + Tối ưu lưu trữ tài nguyên tĩnh trên Amazon S3 và chiến lược cô lập bucket.<br>  + Amazon CloudFront Distribution, Edge Caching, chứng chỉ SSL/TLS tùy chỉnh qua AWS Certificate Manager (ACM).<br>  + Origin Access Control (OAC): Khóa chặt S3 bucket, chỉ cho phép CloudFront truy cập.<br>- **Thực hành:**<br>  + Tạo S3 bucket ở chế độ Private để chứa tài nguyên giao diện ứng dụng Wakan (UI Assets).<br>  + Khởi tạo CloudFront distribution tích hợp OAC, chặn hoàn toàn truy cập trực tiếp từ Internet vào S3 bucket. | 09/06/2026 | 09/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Vành đai Bảo mật Biên với AWS WAF & Ngăn chặn Hiểm họa Mạng**<br>- **Kiến thức:**<br>  + Tường lửa ứng dụng AWS WAF: Web ACLs, Quy tắc tự định nghĩa vs Tập quy tắc AWS Managed Rules (`AWSManagedRulesCommonRuleSet`, SQLi, Known Bad Inputs).<br>  + Quy tắc Rate-based giới hạn tần suất truy cập ngăn chặn tấn công HTTP Flood / DDoS tại biên mạng.<br>- **Thực hành:**<br>  + Khởi tạo AWS WAF Web ACL gán trực tiếp vào CloudFront Distribution của dự án Wakan.<br>  + Thiết lập quy tắc rate-limiting (giới hạn 100 requests / 5 phút per IP) và kích hoạt theo dõi log WAF. | 10/06/2026 | 10/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Quản lý Định danh & Xác thực Người dùng với Amazon Cognito**<br>- **Kiến thức:**<br>  + Amazon Cognito User Pools vs Identity Pools, luồng xác thực OAuth 2.0 / OIDC.<br>  + Vòng đời JWT Token: ID Tokens, Access Tokens, Refresh Tokens.<br>  + Cấu hình User Pool Client, bắt buộc bảo mật MFA và thuộc tính người dùng tùy chỉnh.<br>- **Thực hành:**<br>  + Khởi tạo Amazon Cognito User Pool cho Wakan hỗ trợ đăng ký và xác thực tài khoản qua Email.<br>  + Cấu hình các thuộc tính người dùng tùy chỉnh (phong cách du lịch yêu thích, ngân sách) và tích hợp Hosted UI. | 11/06/2026 | 11/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: IAM Execution Roles Đặc quyền Tối thiểu & Hàng rào Bảo mật cho AWS Lambda**<br>- **Kiến thức:**<br>  + Phân quyền chi tiết IAM execution roles cho các hàm AWS Lambda.<br>  + Từ khóa điều kiện trong chính sách IAM (`aws:PrincipalOrgID`, `s3:ResourceAccount`, `dynamodb:LeadingKeys`).<br>  + Nguyên tắc Đặc quyền Tối thiểu (Least-Privilege) và chính sách gán trực tiếp theo tài nguyên.<br>- **Thực hành:**<br>  + Viết các chính sách IAM execution policy dạng JSON chặt chẽ cho các hàm Lambda dự án Wakan, chỉ giới hạn quyền trong ARN bảng DynamoDB và khóa Secrets Manager quy định.<br>  + Kiểm tra tính hợp lệ của phân quyền bằng công cụ IAM Policy Simulator. | 12/06/2026 | 12/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 8:

#### Thứ Hai (08/06/2026):
* Thống nhất tài liệu định nghĩa API Contract chuẩn RESTful cho toàn hệ thống dự án Wakan sử dụng chuẩn OpenAPI 3.0.
* Chuẩn hóa cấu trúc dữ liệu JSON đầu vào cho các sở thích du lịch người dùng và dữ liệu đầu ra cho lịch trình do AI khởi tạo.
* Quy định danh mục mã lỗi tiêu chuẩn giúp phía Client (Frontend) dễ dàng bắt lỗi và hiển thị thông báo phù hợp.

#### Thứ Ba (09/06/2026):
* Triển khai thành công Amazon S3 Bucket ở chế độ cô lập hoàn toàn để lưu trữ mã nguồn giao diện động của Wakan.
* Khởi tạo mạng phân phối nội dung Amazon CloudFront CDN giúp tăng tốc độ tải trang cho người dùng với độ trễ tối thiểu.
* Khóa chặt S3 Origin bằng cơ chế Origin Access Control (OAC), triệt tiêu nguy cơ lộ dữ liệu giao diện tĩnh ra ngoài Internet.

#### Thứ Tư (10/06/2026):
* Xây dựng vành đai bảo mật biên kiên cố bằng cách triển khai AWS WAF Web ACL bao bọc CloudFront.
* Kích hoạt bộ quy tắc AWS Managed Rules chặn đứng các lỗ hổng an ninh mạng phổ biến (OWASP Top 10, SQL Injection, Cross-Site Scripting).
* Cấu hình quy tắc giới hạn truy cập theo tần suất (Rate-based rules) chống lại botnet và tấn công từ chối dịch vụ (DDoS) vào cổng backend.

#### Thứ Năm (11/06/2026):
* Khởi tạo Amazon Cognito User Pools chịu trách nhiệm quản lý toàn bộ luồng đăng ký, đăng nhập và xác thực cho người dùng Wakan.
* Kích hoạt tính năng xác thực tài khoản qua Email, chính sách mật khẩu mạnh và sẵn sàng cho xác thực hai lớp (MFA).
* Lưu trữ trực tiếp các thuộc tính sở thích du lịch cá nhân vào token Cognito, giúp ứng dụng cá nhân hóa trải nghiệm người dùng nhanh chóng.

#### Thứ Sáu (12/06/2026):
* Tự tay viết các chính sách IAM Execution Role chi tiết cho từng hàm Lambda backend tuân thủ Nguyên tắc Đặc quyền Tối thiểu.
* Chặn đứng nguy cơ vượt quyền bằng cách giới hạn chính xác ARN bảng DynamoDB và ARN chuỗi mật khẩu trong Secrets Manager mà Lambda được phép truy vấn.
* Sử dụng công cụ IAM Policy Simulator để kiểm thử và xác nhận các hàm Lambda không có quyền hạn dư thừa.