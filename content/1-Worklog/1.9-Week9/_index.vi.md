---
title: "Worklog Tuần 9"
date: 2026-06-15
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:
* Bảo mật các thông tin nhạy cảm (API Keys) phục vụ cho quá trình xử lý AI.
* Thiết lập giới hạn truy cập API để chống spam và lạm dụng tài nguyên.
* Rà soát chính sách bảo mật và review chéo mã nguồn toàn hệ thống.

### Các công việc đã hoàn thành:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái |
| --- | --- | --- | --- | --- |
| 2 | - Review chéo code đảm bảo logic nghiệp vụ và bảo mật | 15/06/2026 | 15/06/2026 | Hoàn thành |
| 3 | - Cấu hình AWS Secrets Manager lưu trữ External AI API Key | 16/06/2026 | 16/06/2026 | Hoàn thành |
| 4 | - Thiết lập API Gateway Usage Plans | 17/06/2026 | 17/06/2026 | Hoàn thành |
| 5 | - Cấu hình Rate limit chặn spam API | 18/06/2026 | 18/06/2026 | Hoàn thành |
| 6 | - Rà soát toàn bộ chính sách bảo mật & Họp Architecture Review | 19/06/2026 | 19/06/2026 | Hoàn thành |

### Kết quả đạt được:
* **Quản lý thông tin nhạy cảm:** Triển khai AWS Secrets Manager, loại bỏ hoàn toàn việc lưu trữ cứng (hardcode) API Key của bên thứ 3 trong mã nguồn.
* **Kiểm soát lưu lượng:** Bảo vệ thành công Backend thông qua việc áp dụng Usage Plans và Rate Limiting trên API Gateway.