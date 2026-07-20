---
title: "Nhật ký Tuần 1"
date: 2026-04-20
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Mục tiêu Tuần 1:
* Nắm vững các dịch vụ cốt lõi của AWS bao gồm Máy chủ (EC2, Lightsail), Lưu trữ (S3), Cơ sở dữ liệu (RDS) và Mạng (VPC, Route 53).
* Thành thạo quản lý phân quyền an toàn với IAM, giám sát hệ thống với CloudWatch và kiểm soát chi phí bằng AWS Budgets.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: AWS Console, Cấu hình CLI & Quản lý truy cập (IAM)**<br>- **Kiến thức:**<br>  + Phân biệt Xác thực (Authentication) & Phân quyền (Authorization) trên AWS.<br>  + Các thành phần IAM: Users, Groups, Roles, và IAM Policies dạng JSON (Nguyên tắc Đặc quyền Tối thiểu).<br>  + Giao diện dòng lệnh AWS CLI & Truy cập lập trình (Access Key ID & Secret Access Key).<br>- **Thực hành:**<br>  + Cấu hình AWS CLI trên máy cục bộ (`aws configure`).<br>  + Tạo IAM User, bật bảo mật MFA và thiết lập IAM Group với chính sách truy cập cụ thể. | 20/04/2026 | 20/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Mạng cơ bản với Amazon VPC & Máy chủ EC2 / Auto Scaling**<br>- **Kiến thức:**<br>  + Kiến trúc Amazon VPC: Subnets (Public/Private), Internet Gateway (IGW), Route Tables, Security Groups (Stateful) & NACLs (Stateless).<br>  + Nền tảng Amazon EC2: Instance types, AMIs, Key Pairs, lưu trữ EBS.<br>  + Khái niệm Độ sẵn sàng cao: Elastic Load Balancing (ELB) & Auto Scaling Groups (ASG).<br>- **Thực hành:**<br>  + Xây dựng VPC tùy chỉnh với Public/Private subnets, IGW và Route Tables.<br>  + Khởi tạo máy chủ EC2 trong public subnet và kết nối SSH thành công. | 21/04/2026 | 21/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Lưu trữ với Amazon S3 & Cơ sở dữ liệu quan hệ Amazon RDS**<br>- **Kiến thức:**<br>  + Amazon S3: Lưu trữ đối tượng, Buckets, Storage Classes, Bucket Policies, Host website tĩnh.<br>  + Amazon RDS: Dịch vụ CSDL quan hệ quản lý tập trung (MySQL/PostgreSQL), triển khai Multi-AZ, Automated Backups & Snapshots.<br>- **Thực hành:**<br>  + Tạo S3 Bucket, cấu hình Bucket Policy cho phép truy cập công khai và host website tĩnh.<br>  + Khởi tạo CSDL Amazon RDS MySQL và kết nối từ máy chủ EC2. | 22/04/2026 | 22/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Đơn giản hóa máy chủ với Amazon Lightsail & Giám sát hệ thống với CloudWatch**<br>- **Kiến thức:**<br>  + Amazon Lightsail: Giải pháp máy chủ ảo (VPS) đóng gói sẵn cho ứng dụng nhỏ và vừa.<br>  + Amazon CloudWatch: Metrics, CloudWatch Logs, Alarms và Dashboards.<br>- **Thực hành:**<br>  + Triển khai nhanh trang WordPress trên Amazon Lightsail và gán IP tĩnh (Static IP).<br>  + Thiết lập CloudWatch Alarm cảnh báo khi CPU EC2 vượt ngưỡng 80% kèm thông báo qua email (SNS). | 23/04/2026 | 23/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Tên miền Route 53 & Quản trị chi phí với AWS Budgets**<br>- **Kiến thức:**<br>  + Amazon Route 53: Hệ thống phân giải tên miền (DNS), Public/Private Hosted Zones, Routing Policies (Simple, Weighted, Failover).<br>  + Quản trị chi phí AWS: AWS Budgets, Cost Allocation Tags, Billing Dashboard.<br>- **Thực hành:**<br>  + Tạo Hosted Zone trên Route 53, trỏ bản ghi A/CNAME về S3 website / EC2.<br>  + Cấu hình AWS Budgets gửi cảnh báo email khi chi phí dự báo vượt 80% ngân sách. | 24/04/2026 | 24/04/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 1:

#### Thứ Hai (20/04/2026):
* Hiểu rõ nguyên lý quản lý định danh trong AWS IAM (Users, Groups, Roles, Policies).
* Thực hành tốt bảo mật tài khoản bằng cách kích hoạt Xác thực 2 lớp (MFA) cho Root và IAM Account.
* Cài đặt và cấu hình thành công AWS CLI trên máy tính cá nhân bằng Access Keys.

#### Thứ Ba (21/04/2026):
* Nắm vững kiến trúc mạng đám mây với Amazon VPC (Subnets, IGW, Route Tables, Security Groups).
* Xây dựng thành công hạ tầng VPC tùy chỉnh với các phân lớp mạng cô lập.
* Khởi tạo thành công máy chủ EC2, gắn ổ đĩa EBS và truy cập SSH thông qua Key Pair.
* Hiểu cách kết hợp EC2 Auto Scaling và Load Balancer để đảm bảo hệ thống tự động co giãn.

#### Thứ Tư (22/04/2026):
* Làm chủ dịch vụ lưu trữ đối tượng Amazon S3, phân quyền truy cập Bucket Policy và vòng đời dữ liệu.
* Triển khai thành công ứng dụng web tĩnh trực tiếp trên Amazon S3.
* Khởi tạo cơ sở dữ liệu quan hệ managed bằng Amazon RDS (MySQL) hỗ trợ Multi-AZ.
* Cấu hình Security Group cho phép ứng dụng EC2 kết nối an toàn tới RDS.

#### Thứ Năm (23/04/2026):
* Phân biệt được sự khác nhau giữa Amazon EC2 và Amazon Lightsail trong việc tối ưu thời gian triển khai.
* Triển khai nhanh trang web WordPress hoàn chỉnh trên Amazon Lightsail chỉ trong vài phút.
* Nắm vững khả năng giám sát hệ thống của Amazon CloudWatch (Metrics, Logs, Alarms).
* Tạo cảnh báo CloudWatch Alarm tự động gửi email thông báo qua Amazon SNS khi CPU quá tải.

#### Thứ Sáu (24/04/2026):
* Hiểu cách quản lý hệ thống tên miền DNS với Amazon Route 53 và các chiến lược định tuyến traffic.
* Trỏ bản ghi tên miền (A/CNAME) thành công về các tài nguyên ứng dụng trên AWS.
* Thiết lập rào cản kiểm soát tài chính tự động bằng AWS Budgets để gửi cảnh báo sớm, tránh phát sinh chi phí ngoài ý muốn.