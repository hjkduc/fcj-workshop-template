---
title: "Nhật ký Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu Tuần 10:
* Thực hiện kiểm thử tích hợp toàn luồng (End-to-End) trên toàn bộ các vi dịch vụ đám mây của dự án Wakan.
* Thiết lập hệ thống giám sát tập trung và theo dõi vận hành sử dụng Amazon CloudWatch Logs và CloudWatch Alarms.
* Triển khai hàng rào kiểm soát tài chính FinOps bằng AWS Budgets và thông báo SNS để bảo vệ nguồn credit được cấp.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Kiểm thử Tích hợp Toàn luồng (End-to-End Full System Test)**<br>- **Kiến thức:**<br>  + Phương pháp kiểm thử tích hợp End-to-End cho kiến trúc Serverless phân tách.<br>  + Phân tích luồng vết dữ liệu qua CloudFront -> API Gateway -> Cognito -> Lambda (Orchestrator & AI Processor) -> DynamoDB.<br>  + Kiểm thử các kịch bản biên: Lỗi xác thực, quá hạn API, logic Cache Hit/Miss.<br>- **Thực hành:**<br>  + Chạy giả lập toàn bộ hành trình người dùng (Đăng ký, đăng nhập, chọn sở thích, tạo lịch trình AI, lấy dữ liệu cache).<br>  + Đo lường độ trễ toàn luồng và phát hiện các điểm nghẽn hiệu năng khi gọi API AI bên ngoài. | 22/06/2026 | 22/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Giám sát Tập trung & Quản lý Log với CloudWatch Logs**<br>- **Kiến thức:**<br>  + Cấu trúc CloudWatch Log Groups, Log Streams, Chính sách lưu trữ Log (Retention Policy) và định dạng JSON Log.<br>  + Tập trung hóa log hoạt động từ API Gateway, Lambda, Cognito và AWS WAF.<br>  + Truy vấn log đa dịch vụ hiệu quả bằng công cụ CloudWatch Logs Insights.<br>- **Thực hành:**<br>  + Thiết lập thời hạn lưu trữ log 14 ngày cho tất cả Log Groups của Wakan để tối ưu chi phí lưu trữ.<br>  + Viết các câu truy vấn CloudWatch Logs Insights đếm số lượng lỗi API và đo thời gian Cold Start của Lambda. | 23/06/2026 | 23/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Cảnh báo Chủ động, CloudWatch Alarms & Tích hợp Amazon SNS**<br>- **Kiến thức:**<br>  + Amazon CloudWatch Alarms, phép toán chỉ số (metric math), ngưỡng cố định vs mô hình phát hiện bất thường.<br>  + Kênh thông báo cảnh báo kỹ thuật bằng Amazon SNS (Simple Notification Service).<br>  + Các chỉ số đo lường hiệu năng cốt lõi: Tỷ lệ lỗi 5xx trên API Gateway, lỗi thực thi Lambda, DynamoDB Throttling.<br>- **Thực hành:**<br>  + Khởi tạo SNS Topic gửi email cảnh báo tự động tới đội ngũ phát triển.<br>  + Cấu hình CloudWatch Alarms cho ngưỡng lỗi Lambda (>2% failure rate) và mã phản hồi HTTP 5xx từ API Gateway. | 24/06/2026 | 24/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Quản trị Tài chính FinOps, AWS Budgets & Phát hiện Anomaly**<br>- **Kiến thức:**<br>  + Cơ chế kiểm soát chi phí FinOps và theo dõi tốc độ tiêu thụ AWS Credit.<br>  + AWS Budgets: Cảnh báo theo hạn mức cố định hoặc phần trăm, chi phí thực tế vs chi phí dự báo.<br>  + Tích hợp AWS Cost Anomaly Detection tự động nhận diện chi tiêu tăng vọt.<br>- **Thực hành:**<br>  + Cấu hình AWS Budgets gửi email cảnh báo phân cấp khi lượng credit tiêu thụ đạt 50%, 80% và 100%.<br>  + Thiết lập bộ theo dõi AWS Cost Anomaly Detection cho các dịch vụ compute và database của Wakan. | 25/06/2026 | 25/06/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Tối ưu Hiệu năng Serverless & Khắc phục Lỗi Chéo giữa các Nhóm**<br>- **Kiến thức:**<br>  + Tối ưu hóa thời gian Cold Start của AWS Lambda, tinh chỉnh dung lượng RAM và giới hạn concurrency.<br>  + Tinh chỉnh hiệu năng câu lệnh Query vs Scan trên DynamoDB, kiểm tra cơ chế tự dọn dẹp của TTL.<br>- **Thực hành:**<br>  + Sửa các lỗi phát sinh trong đợt kiểm thử E2E (xử lý ngoại lệ JSON và cấu hình CORS Preflight headers).<br>  + Tinh chỉnh cấu hình RAM cho các hàm Lambda giúp giảm thời gian thực thi và tối ưu hóa chi phí. | 26/06/2026 | 26/06/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 10:

#### Thứ Hai (22/06/2026):
* Thực hiện thành công đợt kiểm thử tích hợp toàn luồng (E2E), giả lập chính xác toàn bộ hành trình trải nghiệm của người dùng trên ứng dụng Wakan.
* Kiểm tra tính thông suốt khi dữ liệu truyền từ CloudFront Edge qua API Gateway, xác thực qua Cognito và xử lý tại các hàm Lambda backend.
* Xác nhận cơ chế kiểm tra Cache trên DynamoDB hoạt động chính xác: Các yêu cầu trùng lặp được trả về kết quả ngay tức thì từ Cache mà không tốn chi phí gọi sang API AI bên ngoài.

#### Thứ Ba (23/06/2026):
* Tập trung hóa toàn bộ nhật ký vận hành hệ thống bằng cách cấu hình CloudWatch Log Groups cho API Gateway, Lambda và AWS WAF.
* Áp dụng chính sách tự động xóa log sau 14 ngày cho toàn bộ các dịch vụ, giúp ngăn ngừa tình trạng phình to dung lượng lưu trữ và phát sinh chi phí ngầm.
* Thành thạo công cụ CloudWatch Logs Insights, viết các câu truy vấn dạng SQL để bóc tách thông tin lỗi từ dữ liệu log định dạng JSON.

#### Thứ Tư (24/06/2026):
* Xây dựng mạng lưới cảnh báo vận hành chủ động bằng cách kết hợp CloudWatch Alarms với dịch vụ gửi email thông báo Amazon SNS.
* Thiết lập các bộ cảnh báo tự động kích hoạt khi API Gateway trả về lỗi 5xx Server Error hoặc khi hàm Lambda gặp sự cố không thể thực thi.
* Cấu hình cảnh báo hạn mức đọc/ghi của DynamoDB nhằm kịp thời phát hiện nguy cơ nghẽn dữ liệu khi lưu lượng truy cập tăng cao.

#### Thứ Năm (25/05/2026):
* Bảo vệ an toàn ngân sách dự án bằng cách thiết lập các hạn mức cảnh báo chi tiết trên AWS Budgets để kiểm soát lượng AWS Credit.
* Thiết lập hệ thống tự động gửi email thông báo cho đội ngũ phát triển khi chi phí tiêu thụ thực tế hoặc dự báo đạt ngưỡng 50%, 80% và 100%.
* Kích hoạt AWS Cost Anomaly Detection để hệ thống tự động phát hiện và cảnh báo nếu có sự biến động chi tiêu bất thường trên các dịch vụ Lambda và DynamoDB.

#### Thứ Sáu (26/06/2026):
* Phối hợp giữa các nhóm (Frontend, Backend, AI) để khắc phục triệt để các lỗi phát sinh sau đợt kiểm thử E2E.
* Xử lý thành công lỗi CORS Preflight headers trên API Gateway và chuẩn hóa dữ liệu phản hồi từ các API AI bên ngoài.
* Tinh chỉnh lại dung lượng bộ nhớ RAM gán cho các hàm Lambda, giúp giảm thời gian xử lý trung bình và nâng cao tốc độ phản hồi của toàn hệ thống.