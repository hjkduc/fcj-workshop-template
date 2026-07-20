---
title: "Nhật ký Tuần 7"
date: 2026-06-01
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu Tuần 7:
* Khởi động dự án thực tế **Wakan – Trợ lý du lịch cá nhân hóa bằng AI**, xác định phạm vi sản phẩm và phân cấp tính năng (Free/Plus/Pro).
* Thiết kế hoàn chỉnh kiến trúc đám mây Serverless (Cloud-Native) và khởi tạo môi trường làm việc nhóm (Git, AWS IAM).
* Rà soát bảo mật và đánh giá kiến trúc dựa trên 6 trụ cột của khung chuẩn AWS Well-Architected Framework.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Kickoff Dự án Wakan, Xác định Phạm vi & Thiết lập Môi trường**<br>- **Kiến thức:**<br>  + Lập Yêu cầu sản phẩm (PRD) cho ứng dụng Trợ lý du lịch Wakan.<br>  + Chiến lược phân cấp tính năng (các gói Free, Plus, Pro giới hạn lượt tạo lịch trình và hạn mức AI API).<br>  + Quy hoạch không gian làm việc nhóm và phân quyền kho lưu trữ mã nguồn.<br>- **Thực hành:**<br>  + Chốt văn bản PRD và danh sách tính năng dự án Wakan.<br>  + Khởi tạo GitHub repository và tạo tài khoản IAM User kèm bắt buộc bảo mật MFA cho các thành viên trong nhóm. | 01/06/2026 | 01/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Thiết kế Kiến trúc Đám mây Wakan (Serverless & Microservices)**<br>- **Kiến thức:**<br>  + Mô hình Serverless tách biệt: Phân phối giao diện (S3 + CloudFront + OAC), API (API Gateway + Cognito), Tính toán bất đồng bộ (Lambda + SQS + Step Functions), CSDL (DynamoDB).<br>  + Vành đai bảo mật: Tường lửa AWS WAF Web ACLs, Origin Cloaking và Cô lập VPC.<br>- **Thực hành:**<br>  + Vẽ và chốt sơ đồ kiến trúc tổng thể dự án Wakan trên công cụ Draw.io.<br>  + Thiết kế danh sách REST API endpoints, định dạng dữ liệu Request/Response và cấu trúc bảng DynamoDB. | 02/06/2026 | 02/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Đánh giá Kiến trúc theo AWS Well-Architected Framework**<br>- **Kiến thức:**<br>  + 6 Trụ cột chuẩn hóa: Bảo mật (Security), Vận hành xuất sắc (Operational Excellence), Độ tin cậy (Reliability), Hiệu năng (Performance Efficiency), Tối ưu chi phí (Cost Optimization), Độ bền vững (Sustainability).<br>  + Đi sâu trụ cột Bảo mật: Phân quyền đặc quyền tối thiểu, mã hóa dữ liệu (at-rest / in-transit), bảo vệ biên mạng.<br>- **Thực hành:**<br>  + Thực hiện đánh giá kiến trúc Wakan bằng công cụ AWS Well-Architected Tool.<br>  + Nhận diện các rủi ro kỹ thuật cao (HRI) và lập lộ trình khắc phục cho tầng xác thực và các cổng API. | 03/06/2026 | 03/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Thiết lập IAM Roles, Policies & Hàng rào Bảo mật (Guardrails)**<br>- **Kiến thức:**<br>  + Cấu trúc cú pháp IAM Policy: Effect, Action, Resource, Conditions.<br>  + IAM Execution Roles liên dịch vụ (Lambda execution roles, API Gateway logging roles).<br>  + Nguyên tắc Đặc quyền Tối thiểu (Least-Privilege) và ranh giới phân quyền (Permission Boundaries).<br>- **Thực hành:**<br>  + Soạn thảo các chính sách IAM execution policy dạng JSON cho Lambda với quyền hạn tối thiểu tới DynamoDB và Secrets Manager.<br>  + Cấu hình kho lưu trữ AWS Secrets Manager để quản lý API Key của dịch vụ AI bên ngoài. | 04/06/2026 | 04/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Họp Nhóm, Bảo vệ Kiến trúc với Mentors & Chốt Hạ tầng**<br>- **Kiến thức:**<br>  + Kỹ năng trình bày giải pháp kỹ thuật và lập tài liệu quyết định kiến trúc (ADR).<br>  + Tiếp thu và tối ưu giải pháp dựa trên phản hồi của Chuyên gia giải pháp (Solutions Architect).<br>- **Thực hành:**<br>  + Trình bày thiết kế kiến trúc Wakan và báo cáo Well-Architected trước các Mentor AWS.<br>  + Tiếp thu góp ý về mô hình xử lý bất đồng bộ và nhận xác nhận (sign-off) thông qua kiến trúc chính thức. | 05/06/2026 | 05/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 7:

#### Thứ Hai (01/06/2026):
* Khởi động thành công dự án thực tế **Wakan (Trợ lý du lịch cá nhân hóa bằng AI)**, thống nhất phạm vi sản phẩm và phân cấp tính năng các gói dịch vụ (Free, Plus, Pro).
* Khởi tạo kho lưu trữ mã nguồn nhóm trên GitHub kèm quy tắc bảo vệ nhánh (Branch Protection Rules).
* Cấp phát tài khoản IAM User cá nhân tích hợp bắt buộc xác thực 2 lớp (MFA) và thiết lập ranh giới phân quyền ban đầu cho toàn đội.

#### Thứ Ba (02/06/2026):
* Hoàn thiện sơ đồ kiến trúc đám mây Serverless tổng thể cho Wakan tích hợp CloudFront, S3, API Gateway, Cognito, Lambda, DynamoDB và AWS WAF.
* Thiết kế danh sách thông số các REST API và mô hình hóa cấu trúc dữ liệu lưu trữ lịch trình du lịch, thông tin người dùng và bộ nhớ cache.
* Ánh xạ chi tiết luồng di chuyển dữ liệu giữa các cổng API, bộ xác thực Cognito và các hàm xử lý Lambda.

#### Thứ Tư (03/06/2026):
* Thực hiện bài đánh giá kiến trúc Wakan dựa trên 6 trụ cột của AWS Well-Architected Framework bằng công cụ AWS Well-Architected Tool.
* Nhận diện điểm nghẽn độ trễ khi gọi đồng bộ sang các API AI bên ngoài, từ đó đưa ra phương án dự phòng bằng hàng đợi xử lý bất đồng bộ.
* Thiết lập tiêu chuẩn bảo mật bắt buộc mã hóa toàn bộ dữ liệu khi truyền tải (HTTPS/TLS) và khi lưu trữ (KMS).

#### Thứ Năm (04/06/2026):
* Tạo các chính sách IAM Execution Role phân quyền chi tiết cho các hàm Lambda tuân thủ nghiêm ngặt Nguyên tắc Đặc quyền Tối thiểu.
* Cấu hình dịch vụ AWS Secrets Manager lưu trữ bảo mật các chuỗi API Token của mô hình AI đối tác, loại bỏ hoàn toàn việc lưu mật khẩu trong mã nguồn.
* Định nghĩa chính sách phân quyền ghi log lên Amazon CloudWatch cho môi trường thực thi API Gateway và Lambda.

#### Thứ Sáu (05/06/2026):
* Bảo vệ thành công sơ đồ kiến trúc Wakan và báo cáo Well-Architected Review trước hội đồng Mentor AWS Việt Nam.
* Nhận đánh giá tích cực về chiến lược bảo mật và tối ưu kiến trúc xử lý lịch trình du lịch bằng AI.
* Nhận chữ ký phê duyệt (sign-off) kiến trúc chính thức, sẵn sàng bước vào giai đoạn dựng hạ tầng và lập trình các tính năng trong tuần tiếp theo.