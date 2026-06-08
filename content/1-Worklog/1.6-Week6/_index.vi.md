---
title: "Worklog Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:

* Triển khai các biện pháp Bảo mật (Security) toàn diện cho định danh, dữ liệu và mạng lưới.
* Nâng cao Độ tin cậy (Reliability) thông qua tính sẵn sàng cao (HA) và sao lưu tự động.
* Làm chủ mạng doanh nghiệp và các kiến trúc chịu lỗi phức tạp.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2 | - Liên kết danh tính (AWS SSO) & Xác thực liên miền (Cognito) <br> - Kiểm soát quyền với IAM Permission Boundaries, Policies & Conditions | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | - Tuân thủ với Security Hub & Giám sát với GuardDuty <br> - Bảo vệ dữ liệu với KMS, Macie, Secrets Manager <br> - Bảo vệ ứng dụng với WAF & Firewall Manager | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | - Truy cập riêng tư đến S3 với VPC Endpoints & Best practices cho S3 <br> - Vá lỗi hệ thống với EC2 Image Builder | 27/05/2026 | 27/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | - Bảo vệ dữ liệu với AWS Backup <br> - Tích hợp mạng: VPC Peering & Transit Gateway <br> - Hệ thống nhắn tin SQS và SNS | 28/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | - Chia sẻ lưu trữ với EBS Multi-Attach <br> - Cụm chịu lỗi Windows Server & SQL Server tính sẵn sàng cao (2019/2022) | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

### Kết quả đạt được tuần 6:

* **Bảo mật toàn diện:** Vận dụng các lớp bảo mật đa tầng (WAF, KMS, Macie, Secrets Manager) và kiểm soát định danh chặt chẽ (SSO, Cognito). Giám sát rủi ro tự động qua Security Hub và GuardDuty.
* **Mạng và Lưu trữ an toàn:** Cấu hình truy cập S3 không qua Internet bằng VPC Endpoints và tự động hóa vá lỗi máy chủ thông qua EC2 Image Builder.
* **Độ tin cậy hạ tầng:** Thiết kế mạng diện rộng bằng Transit Gateway, VPC Peering và phân tách hệ thống để tăng khả năng chịu lỗi với SQS, SNS.
* **Sẵn sàng cao (HA):** Nắm vững kỹ thuật dự phòng (AWS Backup, EBS Multi-Attach) và thiết lập môi trường Cluster/HA cho Windows Server và SQL Server.