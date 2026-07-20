---
title: "Nhật ký Tuần 4"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu Tuần 4:
* Thành thạo đóng gói ứng dụng với Docker và điều phối container sử dụng Amazon ECS kết hợp cơ chế điện toán phi máy chủ AWS Fargate.
* Nắm vững nền tảng Kubernetes qua Amazon EKS, tự động hóa khởi tạo cụm với EKS Blueprints và tìm hiểu giải pháp container doanh nghiệp Red Hat OpenShift Service on AWS (ROSA).
* Triển khai luồng CI/CD tự động theo văn hóa DevOps và điều phối luồng ứng dụng vi dịch vụ phức tạp bằng AWS Step Functions.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Container hóa với Docker & Điều phối bằng Amazon ECS & AWS Fargate**<br>- **Kiến thức:**<br>  + Nền tảng Docker: Images, Containers, tối ưu Dockerfile, kho lưu trữ Amazon Elastic Container Registry (ECR).<br>  + Khái niệm cốt lõi Amazon ECS: Clusters, Task Definitions, Tasks, Services.<br>  + Môi trường thực thi: EC2 Launch Type vs Điện toán phi máy chủ AWS Fargate.<br>- **Thực hành:**<br>  + Đóng gói ứng dụng web thành Docker image và đẩy lên Amazon ECR.<br>  + Khởi tạo cụm Amazon ECS và triển khai ứng dụng chạy trên nền tảng Serverless AWS Fargate. | 11/05/2026 | 11/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: CI/CD Pipeline cho ECS với AWS CodePipeline & IaC cho ECS dùng CDK**<br>- **Kiến thức:**<br>  + Bộ công cụ DevOps AWS: CodeCommit, CodeBuild, CodeDeploy, CodePipeline.<br>  + Triển khai tự động: Cập nhật cuộn (Rolling updates), chiến lược Blue/Green cho ECS.<br>  + High-Level CDK Construct: `ApplicationLoadBalancedFargateService`.<br>- **Thực hành:**<br>  + Xây dựng luồng CI/CD tự động với CodePipeline để build image và deploy lên ECS Fargate mỗi khi có code mới.<br>  + Viết mã CDK khởi tạo tự động cụm ECS Fargate nằm sau Application Load Balancer. | 12/05/2026 | 12/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Bắt đầu với Amazon EKS (Kubernetes) & EKS Blueprints cho CDK**<br>- **Kiến thức:**<br>  + Kiến trúc Kubernetes: Control Plane, Worker Nodes, Pods, Deployments, Services, Ingress.<br>  + Amazon EKS Managed Kubernetes: Managed Node Groups, Fargate profiles, kết nối công cụ `kubectl`.<br>  + EKS Blueprints for CDK: Bộ công cụ khởi tạo nhanh cụm EKS chuẩn hóa cho môi trường Production.<br>- **Thực hành:**<br>  + Khởi tạo cụm Amazon EKS tự động bằng EKS Blueprints for CDK.<br>  + Triển khai ứng dụng mẫu lên cụm EKS và public ra ngoài qua dịch vụ LoadBalancer bằng `kubectl`. | 13/05/2026 | 13/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: CI/CD cho ứng dụng EKS & Red Hat OpenShift Service trên AWS (ROSA)**<br>- **Kiến thức:**<br>  + Chiến lược triển khai ứng dụng Kubernetes: Mô hình GitOps (ArgoCD/Flux) vs AWS CodePipeline cho EKS.<br>  + Red Hat OpenShift Service on AWS (ROSA): Kiến trúc OpenShift doanh nghiệp managed, tích hợp đám mây lai và tuân thủ bảo mật.<br>- **Thực hành:**<br>  + Cấu hình luồng CI/CD tự động cập nhật các file Kubernetes manifest lên cụm EKS.<br>  + Nghiên cứu mô hình triển khai ROSA và các kịch bản chuyển dịch hạ tầng doanh nghiệp lớn. | 14/05/2026 | 14/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Lưu trữ lai Storage Gateway, Amazon FSx & Điều phối quy trình với Step Functions**<br>- **Kiến thức:**<br>  + AWS Storage Gateway: Volume Gateway, Tape Gateway, S3 File Gateway cho lưu trữ đám mây lai (Hybrid Cloud).<br>  + Hệ sinh thái Amazon FSx: FSx cho Windows File Server, Lustre, NetApp ONTAP, OpenZFS.<br>  + AWS Step Functions: State Machines, điều phối luồng trực quan, xử lý lỗi (error handling), retry và chạy song song.<br>- **Thực hành:**<br>  + Xây dựng State Machine trên AWS Step Functions để điều phối luồng xử lý bất đồng bộ giữa các vi dịch vụ.<br>  + Đánh giá các giải pháp lưu trữ Amazon FSx cho các bài toán hiệu năng cao. | 15/05/2026 | 15/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 4:

#### Thứ Hai (11/05/2026):
* Làm chủ quy trình đóng gói ứng dụng bằng Docker, tối ưu hóa tệp Dockerfile và quản lý kho lưu trữ hình ảnh trên Amazon ECR.
* Nắm vững các khái niệm điều phối container trong Amazon ECS (Clusters, Task Definitions, Services).
* Loại bỏ hoàn toàn gánh nặng quản lý máy chủ và hệ điều hành bằng cách chạy container trực tiếp trên AWS Fargate.

#### Thứ Ba (12/05/2026):
* Xây dựng thành công luồng CI/CD tự động với AWS CodePipeline để tự động build Docker image và cập nhật ứng dụng trên ECS không gây gián đoạn dịch vụ (Zero-Downtime).
* Lập trình khởi tạo hạ tầng ECS Fargate có tích hợp Load Balancer chỉ với vài dòng mã bằng AWS CDK.
* Hiểu chiến lược triển khai Blue/Green deployment qua AWS CodeDeploy áp dụng cho các ứng dụng quan trọng.

#### Thứ Tư (13/05/2026):
* Nắm vững các thành phần cốt lõi của Kubernetes (Control Plane, Nodes, Pods, Deployments, Services).
* Khởi tạo cụm Amazon EKS chuẩn doanh nghiệp một cách nhanh chóng nhờ công cụ EKS Blueprints for CDK.
* Thực hành sử dụng lệnh `kubectl` để quản trị, kiểm tra và public dịch vụ ứng dụng trên cụm EKS.

#### Thứ Năm (14/05/2026):
* Nghiên cứu các phương pháp tự động hóa đống triển khai ứng dụng Kubernetes, so sánh giữa tư duy GitOps và CI/CD truyền thống.
* Hiểu rõ ưu thế của giải pháp container chuẩn doanh nghiệp Red Hat OpenShift Service on AWS (ROSA).
* Phân tích mô hình kiến trúc đám mây lai phù hợp cho việc chuyển dịch ứng dụng của các tập đoàn lớn.

#### Thứ Sáu (15/05/2026):
* Đánh giá các giải pháp lưu trữ lai với AWS Storage Gateway và bộ giải pháp lưu trữ hiệu năng cao Amazon FSx.
* Làm chủ công cụ điều phối quy trình vi dịch vụ (Microservices Orchestration) bằng AWS Step Functions.
* Xây dựng luồng công việc dạng đồ họa trực quan có khả năng tự động xử lý lỗi, phân nhánh điều kiện và thực thi tác vụ song song.