---
title: "Nhật ký Tuần 5"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu Tuần 5:
* Nghiên cứu phương pháp luận kiến trúc đám mây hiện đại, chuyển dịch ứng dụng Monolith truyền thống sang hệ thống Microservices hướng sự kiện (Event-driven).
* Xây dựng hoàn chỉnh ứng dụng Serverless Full-stack (Serverless Book Store) kết hợp AWS Lambda, Amazon DynamoDB, Amazon S3 và API Gateway.
* Làm chủ cơ chế truyền tin bất đồng bộ (SNS, SQS, EventBridge) và tích hợp API GraphQL linh hoạt bằng AWS AppSync.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Chuyển dịch sang Microservices & Nền tảng Kiến trúc Hướng sự kiện (EDA)**<br>- **Kiến thức:**<br>  + Monolith vs Microservices: Lợi ích, thách thức, Thiết kế hướng tên miền (DDD), mẫu thiết kế Strangler Fig.<br>  + Kiến trúc hướng sự kiện (Event-Driven Architecture): Event Producers, Event Routers (Amazon EventBridge), Event Consumers, Schema Registry.<br>- **Thực hành:**<br>  + Lập lộ trình tách nhỏ ứng dụng Monolith thành các Microservices bằng Strangler Fig pattern và EventBridge rules. | 18/05/2026 | 18/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Xác thực ứng dụng SPA & Tích hợp dịch vụ AWS AI**<br>- **Kiến thức:**<br>  + Bảo mật ứng dụng trang đơn (SPA): Luồng xác thực OAuth 2.0 / OIDC, xử lý JWT token và cấu hình CORS.<br>  + Các dịch vụ AWS AI dựng sẵn: Amazon Rekognition (Thị giác máy tính), Polly (Chuyển văn bản thành giọng nói), Translate, Transcribe.<br>- **Thực hành:**<br>  + Xây dựng giao diện Web gọi các dịch vụ AWS AI (Polly & Translate) thông qua cổng API bảo mật. | 19/05/2026 | 19/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Serverless Book Store: Backend với Lambda, S3 & DynamoDB**<br>- **Kiến thức:**<br>  + Mẫu ứng dụng Serverless: Thiết kế RESTful API bằng Amazon API Gateway.<br>  + DynamoDB Single-Table Design: Mô hình thiết kế một bảng, tối ưu Access Patterns, Primary Keys và Secondary Indexes.<br>  + Lưu trữ S3: Host tệp tĩnh và cấu hình quy tắc CORS.<br>- **Thực hành:**<br>  + Phát triển các API CRUD cốt lõi cho ứng dụng Book Store bằng API Gateway, Lambda và DynamoDB. | 20/05/2026 | 20/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Tích hợp Frontend, Triển khai AWS SAM & Xác thực người dùng Cognito**<br>- **Kiến thức:**<br>  + Hạ tầng dưới dạng mã cho Serverless: Mẫu dựng AWS SAM (Serverless Application Model), quy trình SAM CLI (`sam build`, `sam deploy`).<br>  + Xác thực người dùng: Amazon Cognito User Pools, Hosted UI và API Gateway Cognito Authorizer.<br>- **Thực hành:**<br>  + Triển khai toàn bộ ứng dụng Book Store Full-stack bằng công cụ AWS SAM CLI.<br>  + Tích hợp Amazon Cognito User Pool để bảo mật các tuyến API Backend bằng kiểm tra JWT token. | 21/05/2026 | 21/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Xử lý sự kiện bất đồng bộ (SQS/SNS) & API GraphQL với AWS AppSync**<br>- **Kiến thức:**<br>  + Tách rời hệ thống (Decoupling): Amazon SNS (Pub/Sub) vs Amazon SQS (Message Queue, Dead Letter Queue - DLQ), mô hình Fan-out.<br>  + API GraphQL: So sánh REST vs GraphQL, AWS AppSync Schema, Data Sources và Resolvers.<br>- **Thực hành:**<br>  + Xây dựng pipeline xử lý đơn hàng bất đồng bộ bằng mô hình SNS Fan-out sang các hàng đợi SQS.<br>  + Triển khai API GraphQL bằng AWS AppSync kết nối truy vấn dữ liệu từ bảng DynamoDB. | 22/05/2026 | 22/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 5:

#### Thứ Hai (18/05/2026):
* Nắm vững chiến lược tách nhỏ hệ thống Monolith sang kiến trúc Microservices linh hoạt bằng Domain-Driven Design và mẫu thiết kế Strangler Fig.
* Hiểu rõ nguyên lý cốt lõi của Kiến trúc Hướng sự kiện (EDA) và khả năng điều phối sự kiện linh hoạt của Amazon EventBridge.
* Thiết kế bản vẽ tích hợp hướng sự kiện giúp phân tách các thành phần legacy mà không gây gián đoạn hệ thống đang vận hành.

#### Thứ Ba (19/05/2026):
* Thành thạo cơ chế bảo mật xác thực cho ứng dụng trang đơn (SPA) sử dụng chuẩn OAuth 2.0 và JWT tokens.
* Trải nghiệm các dịch vụ AI dựng sẵn của AWS (Polly, Translate, Rekognition) giúp tích hợp tính năng thông minh vào ứng dụng mà không cần huấn luyện mô hình ML.
* Xây dựng thành công ứng dụng Web có khả năng tự động dịch thuật và phát âm thanh từ văn bản qua các API dịch vụ AI.

#### Thứ Tư (20/05/2026):
* Áp dụng kỹ thuật DynamoDB Single-Table Design để tối ưu hóa hiệu năng và chi phí truy vấn dữ liệu cho dự án Book Store.
* Khởi tạo các tuyến API RESTful trên Amazon API Gateway kết nối trực tiếp tới mã xử lý logic trong AWS Lambda.
* Cấu hình Amazon S3 lưu trữ tài nguyên giao diện tĩnh và thiết lập quy tắc CORS an toàn.

#### Thứ Năm (21/05/2026):
* Tự động hóa hoàn toàn quy trình đóng gói và triển khai ứng dụng Serverless bằng bộ công cụ AWS SAM CLI.
* Bảo mật các điểm cuối API Gateway bằng cách tích hợp Amazon Cognito User Pool Authorizers.
* Kết nối giao diện Frontend với luồng xác thực Cognito phục vụ tính năng đăng ký và đăng nhập người dùng.

#### Thứ Sáu (22/05/2026):
* Xây dựng hệ thống truyền tin bất đồng bộ có tính chịu lỗi cao theo mô hình SNS Fan-out tới các hàng đợi SQS kết hợp xử lý lỗi qua Dead Letter Queue (DLQ).
* So sánh ưu nhược điểm giữa REST API và GraphQL API, khởi tạo thành công dịch vụ AWS AppSync.
* Lập trình các bộ phân giải (Resolvers) trong AppSync để truy vấn dữ liệu từ DynamoDB một cách linh hoạt, giảm tối đa dung lượng dữ liệu thừa truyền qua mạng.