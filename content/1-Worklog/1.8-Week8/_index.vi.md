---
title: "Worklog Tuần 8"
date: 2026-06-08
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:
* Triển khai nền móng hạ tầng để lưu trữ ứng dụng Frontend và bảo vệ lưu lượng truy cập.
* Thiết lập hệ thống quản lý định danh và siết chặt quyền hạn cho các dịch vụ Serverless.

### Các công việc đã hoàn thành:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái |
| --- | --- | --- | --- | --- |
| 2 | - Đồng bộ API contract giữa Frontend, Backend và AI | 08/06/2026 | 08/06/2026 | Hoàn thành |
| 3 | - Triển khai S3 hosting và Amazon CloudFront | 09/06/2026 | 09/06/2026 | Hoàn thành |
| 4 | - Cấu hình AWS WAF bảo vệ lớp ứng dụng | 10/06/2026 | 10/06/2026 | Hoàn thành |
| 5 | - Dựng Amazon Cognito User Pool cho luồng đăng nhập | 11/06/2026 | 11/06/2026 | Hoàn thành |
| 6 | - Cấu hình IAM least-privilege cho từng Lambda function | 12/06/2026 | 12/06/2026 | Hoàn thành |

### Kết quả đạt được:
* **Lưu trữ & Phân phối:** Đã dựng xong hạ tầng lưu trữ S3 kết hợp CloudFront để tối ưu tốc độ tải trang, được bảo vệ an toàn bởi tường lửa WAF.
* **Bảo mật & Định danh:** Kết nối thành công hệ thống xác thực người dùng Cognito và áp dụng nguyên tắc đặc quyền tối thiểu (least-privilege) cho toàn bộ Lambda.