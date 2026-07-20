---
title: "Nhật ký Tuần 2"
date: 2026-04-27
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu Tuần 2:
* Tìm hiểu các giải pháp CSDL nâng cao (DynamoDB, ElastiCache), Mạng phân phối nội dung (CloudFront) và chiến lược chuyển dịch dữ liệu/hạ tầng (DMS, Disaster Recovery).
* Triển khai bảo mật toàn diện từ quản lý định danh (Cognito, SSO), bảo vệ dữ liệu (KMS, Macie), phát hiện mối đe dọa (GuardDuty) đến bảo mật tại biên mạng (WAF).
* Thiết kế hệ thống mạng liên kết nhiều VPC có tính sẵn sàng cao, chịu lỗi tốt (Transit Gateway, EBS Multi-Attach).

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: CSDL NoSQL DynamoDB, Caching với ElastiCache & Phân phối nội dung CloudFront**<br>- **Kiến thức:**<br>  + Amazon DynamoDB: CSDL NoSQL key-value, Partition/Sort Keys, Global/Local Secondary Indexes (GSI/LSI), Tự động hết hạn dữ liệu (TTL).<br>  + Amazon ElastiCache: Bộ nhớ đệm In-memory (Redis vs Memcached), Chiến lược Caching (Lazy Loading, Write-Through).<br>  + Amazon CloudFront: Mạng phân phối nội dung CDN, Edge Locations, Cache Behaviors, Origin Access Control (OAC).<br>- **Thực hành:**<br>  + Tạo bảng DynamoDB tích hợp GSI và cơ chế TTL tự động xóa dữ liệu cũ.<br>  + Triển khai CloudFront Distribution kết nối an toàn tới S3 Bucket qua OAC. | 27/04/2026 | 27/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Chuyển dịch máy chủ (VM Import), CSDL (DMS) & Khôi phục sau thảm họa (Disaster Recovery)**<br>- **Kiến thức:**<br>  + Chiến lược dịch chuyển lên Cloud (6 Rs of Migration), AWS Application Migration Service (MGN).<br>  + AWS Database Migration Service (DMS): Replication Instance, Source/Target Endpoints, Schema Conversion Tool (SCT).<br>  + Khôi phục sau thảm họa (DR): Chỉ số RTO & RPO, các chiến lược DR (Backup & Restore, Pilot Light, Warm Standby, Multi-Site Active-Active).<br>- **Thực hành:**<br>  + Khởi tạo AWS DMS replication instance và cấu hình tiến trình đồng bộ dữ liệu từ RDS MySQL sang S3/DynamoDB.<br>  + Thiết kế sơ đồ kiến trúc Pilot Light DR cho ứng dụng doanh nghiệp. | 28/04/2026 | 28/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Quản lý định danh (SSO, Cognito) & Bảo vệ ứng dụng (WAF, Firewall Manager)**<br>- **Kiến thức:**<br>  + IAM Identity Center (AWS SSO) & Identity Boundaries.<br>  + Amazon Cognito: User Pools (Xác thực - Authentication) vs Identity Pools (Phân quyền - Authorization).<br>  + AWS WAF: Tường lửa ứng dụng Web, Web ACLs, Managed Rule Groups, Rate-based Rules.<br>  + AWS Firewall Manager: Quản lý chính sách bảo mật tập trung cho AWS Organizations.<br>- **Thực hành:**<br>  + Tạo Amazon Cognito User Pool hỗ trợ xác thực qua Email và MFA.<br>  + Cấu hình AWS WAF Web ACL chống tấn công SQLi/XSS gán vào Application Load Balancer hoặc CloudFront. | 29/04/2026 | 29/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Bảo mật dữ liệu (KMS, Macie), Phát hiện mối đe dọa (GuardDuty) & Tích hợp mạng (Transit Gateway)**<br>- **Kiến thức:**<br>  + AWS KMS: Mã hóa đối xứng (Symmetric) vs Bất đối xứng (Asymmetric), Envelope Encryption, Customer Managed Keys (CMK).<br>  + Amazon Macie: Tự động quét và phát hiện dữ liệu nhạy cảm PII bằng Machine Learning.<br>  + Amazon GuardDuty: Dịch vụ phát hiện mối đe dọa và hành vi bất thường liên tục.<br>  + AWS Transit Gateway: Bộ điều tuyến trung tâm kết nối nhiều VPC và mạng On-premises theo mô hình Hub-and-Spoke.<br>- **Thực hành:**<br>  + Khởi tạo khóa KMS CMK và cấu hình mã hóa phía máy chủ cho S3 (SSE-KMS).<br>  + Cấu hình AWS Transit Gateway kết nối thông suốt 2 VPC cô lập mà không cần VPC Peering. | 30/04/2026 | 30/04/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Lưu trữ sẵn sàng cao (EBS Multi-Attach) & Cụm máy chủ chịu lỗi doanh nghiệp**<br>- **Kiến thức:**<br>  + Ổ đĩa EBS Provisioned IOPS (io1/io2) với tính năng Multi-Attach.<br>  + Cụm máy chủ chịu lỗi Windows Server Failover Clustering (WSFC) & SQL Server Always On Availability Groups trên AWS.<br>  + FSx for Windows File Server: Hệ thống lưu trữ tệp chia sẻ Multi-AZ.<br>- **Thực hành:**<br>  + Khởi tạo ổ đĩa io2 EBS bật Multi-Attach và mount đồng thời vào nhiều máy chủ EC2.<br>  + Nghiên cứu mô hình kiến trúc triển khai cụm SQL Server Failover Cluster Multi-AZ trên AWS. | 01/05/2026 | 01/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 2:

#### Thứ Hai (27/04/2026):
* Hiểu rõ nguyên lý thiết kế CSDL NoSQL với Amazon DynamoDB, chiến lược chọn Partition Key và cơ chế TTL.
* Nắm vững kiến trúc bộ nhớ đệm In-memory với Amazon ElastiCache (Redis) giúp giảm tải truy vấn cho CSDL.
* Triển khai thành công Amazon CloudFront tích hợp Origin Access Control (OAC), vừa bảo mật S3 Origin vừa tăng tốc phân phối nội dung toàn cầu.

#### Thứ Ba (28/04/2026):
* Phân tích 6 chiến lược dịch chuyển hệ thống (6 Rs) và làm chủ dịch vụ AWS Database Migration Service (DMS).
* Cấu hình thành công pipeline đồng bộ dữ liệu liên tục qua DMS với độ trễ cực thấp.
* Đánh giá các chỉ số RTO và RPO để lựa chọn phương án Khôi phục sau thảm họa (Disaster Recovery) tối ưu (Pilot Light & Warm Standby).

#### Thứ Tư (29/04/2026):
* Đi sâu vào cơ chế quản lý định danh người dùng với IAM Identity Center và Amazon Cognito.
* Xây dựng luồng xác thực đăng nhập/đăng ký an toàn sử dụng Amazon Cognito User Pool.
* Thiết lập tường lửa bảo vệ ứng dụng AWS WAF ngăn chặn các lỗ hổng an ninh mạng phổ biến (OWASP Top 10).

#### Thứ Năm (30/04/2026):
* Thành thạo cơ chế mã hóa dữ liệu Envelope Encryption với AWS KMS Customer Managed Keys (CMK).
* Học cách quét dữ liệu cá nhân nhạy cảm (PII) tự động bằng Amazon Macie và phát hiện sự cố an ninh với Amazon GuardDuty.
* Kết nối mạng liên VPC quy mô lớn bằng AWS Transit Gateway theo mô hình Hub-and-Spoke.

#### Thứ Sáu (01/05/2026):
* Thử nghiệm lưu trữ khối hiệu năng cao với EBS Multi-Attach trên chuẩn đĩa io2.
* Phân tích các mô hình triển khai hạ tầng doanh nghiệp có độ sẵn sàng cao cho Windows Server Failover Clustering (WSFC) và SQL Server.
* Hiểu giải pháp lưu trữ tệp tin chia sẻ doanh nghiệp chuẩn POSIX/SMB với Amazon FSx for Windows File Server.