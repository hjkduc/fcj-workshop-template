---
title: "Nhật ký Tuần 3"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu Tuần 3:
* Tự động hóa quy trình vận hành bằng điện toán phi máy chủ (AWS Lambda) và quản lý hệ thống tập trung với AWS Systems Manager (SSM).
* Làm chủ Hạ tầng dưới dạng mã (Infrastructure as Code - IaC) bằng AWS CloudFormation và bộ công cụ AWS Cloud Development Kit (CDK).
* Nâng cao khả năng giám sát, tự động hóa vòng đời sao lưu dữ liệu và thực hiện phân tích chi phí chuyên sâu (FinOps) bằng Amazon Athena & AWS Glue.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Tự động hóa Serverless với AWS Lambda & Truy cập an toàn qua Systems Manager**<br>- **Kiến thức:**<br>  + AWS Lambda: Mô hình thực thi, triggers, IAM execution roles, biến môi trường, bản chất phi trạng thái (stateless).<br>  + AWS Systems Manager (SSM): Session Manager (truy cập SSH/RDP không cần mở port), Parameter Store (quản lý cấu hình/mật khẩu), Run Command, Patch Manager.<br>- **Thực hành:**<br>  + Viết hàm AWS Lambda tự động kích hoạt khi có tệp tin tải lên S3 Bucket.<br>  + Quản trị và truy cập máy chủ EC2 private an toàn bằng SSM Session Manager không cần mở port 22 inbound. | 04/05/2026 | 04/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Giám sát nâng cao CloudWatch & Grafana & IaC với AWS CloudFormation**<br>- **Kiến thức:**<br>  + CloudWatch nâng cao: Custom metrics, CloudWatch Logs Insights, tích hợp Dashboard với Amazon Managed Grafana.<br>  + AWS CloudFormation: Cấu trúc tệp khai báo (YAML/JSON), Stacks, Parameters, Mappings, Resources, Outputs, Phát hiện sai lệch cấu hình (Stack Drift Detection).<br>- **Thực hành:**<br>  + Viết CloudFormation template chuẩn YAML khởi tạo hạ tầng mạng VPC và máy chủ EC2 tự động.<br>  + Tích hợp chỉ số theo dõi từ CloudWatch lên bảng điều khiển Amazon Managed Grafana. | 05/05/2026 | 05/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: IaC nâng cao với AWS CDK, Tối ưu EC2 & VPC Flow Logs**<br>- **Kiến thức:**<br>  + AWS Cloud Development Kit (CDK): Xây dựng hạ tầng bằng ngôn ngữ lập trình (TypeScript/Python), Constructs (L1, L2, L3), CDK Stacks, lệnh CDK CLI (`cdk synth`, `cdk deploy`).<br>  + EC2 Compute Optimizer: Phân tích và đề xuất tinh chỉnh kích thước máy chủ bằng AI.<br>  + VPC Flow Logs: Giám sát và ghi nhận lưu lượng mạng qua giao diện mạng (ENI).<br>- **Thực hành:**<br>  + Khởi tạo dự án AWS CDK khởi tạo S3 Bucket và DynamoDB Table bằng mã nguồn.<br>  + Kích hoạt VPC Flow Logs, thu thập traffic mạng và truy vấn bằng CloudWatch Logs Insights. | 06/05/2026 | 06/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Tự động hóa sao lưu (EBS Data Lifecycle) & Cấu hình VS Code Toolkit**<br>- **Kiến thức:**<br>  + Amazon Data Lifecycle Manager (DLM): Chính sách quản lý vòng đời sao lưu EBS snapshot tự động.<br>  + AWS Backup: Quản lý chính sách sao lưu tập trung đa dịch vụ AWS.<br>  + AWS Toolkit for VS Code: Công cụ kết nối, kiểm thử và triển khai tài nguyên AWS ngay trong môi trường lập trình.<br>- **Thực hành:**<br>  + Cấu hình chính sách DLM tự động tạo bản chụp EBS snapshot hàng ngày và lưu trữ trong 7 ngày.<br>  + Tích hợp AWS Toolkit trên VS Code và kiểm thử gọi hàm Lambda từ máy cục bộ. | 07/05/2026 | 07/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: FinOps: Savings Plans & Reserved Instances & Phân tích chi phí bằng AWS Glue & Athena**<br>- **Kiến thức:**<br>  + Mô hình cam kết chi phí FinOps: Compute Savings Plans, EC2 Instance Savings Plans vs Reserved Instances (Standard/Convertible).<br>  + Cost & Usage Reports (CUR): Xuất dữ liệu hóa đơn chi tiết ra S3.<br>  + Phân tích dữ liệu lớn Serverless: AWS Glue Data Catalog & Amazon Athena (truy vấn SQL trên tệp hóa đơn).<br>- **Thực hành:**<br>  + Cấu hình xuất báo cáo CUR ra S3, dùng AWS Glue quét schema và thực hiện truy vấn SQL phân tích hóa đơn bằng Amazon Athena. | 08/05/2026 | 08/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 3:

#### Thứ Hai (04/05/2026):
* Hiểu rõ kiến trúc điện toán phi máy chủ (Serverless) theo cơ chế sự kiện (Event-driven) với AWS Lambda.
* Loại bỏ hoàn toàn máy chủ Bastion Host và việc mở port SSH 22 bằng cách áp dụng giải pháp truy cập an toàn qua AWS Systems Manager Session Manager.
* Quản lý tập trung các cấu hình và chuỗi kết nối ứng dụng bảo mật bằng AWS Systems Manager Parameter Store.

#### Thứ Ba (05/05/2026):
* Thành thạo tư duy Hạ tầng dưới dạng mã (IaC) dạng khai báo thông qua mẫu dựng AWS CloudFormation.
* Triển khai các stack hạ tầng có tính tái sử dụng cao và sử dụng tính năng Stack Drift Detection để kiểm soát các thay đổi thủ công.
* Nâng cao năng lực giám sát hệ thống nhờ truy vấn log bằng CloudWatch Logs Insights và trực quan hóa biểu đồ qua Amazon Managed Grafana.

#### Thứ Tư (06/05/2026):
* Chuyển đổi sang lập trình hạ tầng theo hướng đối tượng bằng bộ công cụ AWS Cloud Development Kit (CDK).
* Phân tích các đề xuất từ EC2 Compute Optimizer để lựa chọn đúng kích thước máy chủ, giảm thiểu lãng phí tài nguyên.
* Kích hoạt VPC Flow Logs để kiểm tra chi tiết các luồng lưu lượng truy cập mạng và phát hiện các dấu hiệu bất thường.

#### Thứ Năm (07/05/2026):
* Triển khai giải pháp bảo vệ dữ liệu tự động bằng cách thiết lập chính sách Amazon Data Lifecycle Manager (DLM) cho EBS Snapshots.
* Tìm hiểu cơ chế quản trị sao lưu tập trung toàn hệ thống thông qua dịch vụ AWS Backup.
* Tối ưu hóa hiệu suất lập trình đám mây bằng cách tích hợp tiện ích AWS Toolkit trực tiếp vào môi trường VS Code.

#### Thứ Sáu (08/05/2026):
* Đánh giá các mô hình cam kết sử dụng tài nguyên (Savings Plans và Reserved Instances) để tối ưu hóa chi phí máy chủ dài hạn.
* Cấu hình tính năng AWS Cost & Usage Reports (CUR) để trích xuất dữ liệu hóa đơn chi tiết vào kho lưu trữ Amazon S3.
* Tận dụng sức mạnh của AWS Glue và Amazon Athena để thực hiện các truy vấn SQL trực tiếp trên dữ liệu hóa đơn thô, làm chủ tư duy quản trị tài chính đám mây (FinOps).