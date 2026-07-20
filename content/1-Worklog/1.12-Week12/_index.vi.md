---
title: "Nhật ký Tuần 12"
date: 2026-07-06
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu Tuần 12:
* Hoàn thiện toàn bộ ứng dụng Wakan, chạy kiểm thử tổng duyệt toàn hệ thống, quay video demo sản phẩm chính thức và khóa mã nguồn (code freeze).
* Hoàn thành bộ tài liệu kỹ thuật chuyên sâu về Kiến trúc Đám mây AWS, Bảo mật Thông tin Đa lớp và Quản trị Chi phí FinOps.
* Tiến hành rà soát chất lượng cuối cùng, chỉnh sửa chỉn chu hình thức báo cáo và thực hiện nộp bài báo cáo tốt nghiệp chính thức.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Tổng duyệt Hệ thống (Full System Dry Run) & Kiểm thử Chấp nhận**<br>- **Kiến thức:**<br>  + Tiêu chuẩn đánh giá mức độ sẵn sàng vận hành (Production Readiness) cho kiến trúc Serverless.<br>  + Kiểm thử chấp nhận người dùng (UAT) và đo lường độ trễ toàn luồng qua S3, CloudFront, API Gateway, Lambda và DynamoDB.<br>- **Thực hành:**<br>  + Thực hiện đợt tổng duyệt trực tiếp toàn bộ hệ thống Wakan trên môi trường AWS Production.<br>  + Kiểm tra luồng tạo lịch trình bằng AI thời gian thực, vòng đời token Cognito và tốc độ phản hồi Cache từ DynamoDB. | 06/07/2026 | 06/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Quay Video Demo Sản phẩm Chính thức & Sản xuất Media Showcase**<br>- **Kiến thức:**<br>  + Kỹ thuật sản xuất video báo cáo kỹ thuật nhằm nổi bật kiến trúc đám mây, tính năng bảo mật và hành trình người dùng.<br>  + Mở song song màn hình AWS Console để ghi lại phản xạ tức thì của CloudWatch Metrics và AWS WAF.<br>- **Thực hành:**<br>  + Quay video demo sản phẩm chính thức chất lượng cao giới thiệu toàn bộ tính năng của Trợ lý du lịch Wakan.<br>  + Ghi hình trực tiếp thao tác trên AWS Console chứng minh WAF chặn tấn công, Secrets Manager cấp API Key và CloudWatch ghi log. | 07/07/2026 | 07/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Hoàn thiện Hồ sơ Kỹ thuật Kiến trúc & Bảo mật Đám mây**<br>- **Kiến thức:**<br>  + Tổng hợp tài liệu kỹ thuật chuẩn hóa theo 6 trụ cột AWS Well-Architected Framework.<br>  + Trực quan hóa mô hình Serverless phân tách, bảo mật IAM đặc quyền tối thiểu, tường lửa biên WAF và quản trị ngân sách FinOps.<br>- **Thực hành:**<br>  + Biên soạn tài liệu chi tiết thể hiện kiến trúc Wakan, vành đai bảo mật và kết quả tối ưu chi phí.<br>  + Tổng hợp các chỉ số hạ tầng, biểu đồ tiết kiệm chi phí và kết quả kiểm thử xâm nhập thành các biểu đồ trực quan. | 08/07/2026 | 08/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: Khóa Mã nguồn (Code Freeze), Dọn dẹp Kho lưu trữ & Rà soát Chất lượng**<br>- **Kiến thức:**<br>  + Quy trình quản lý phiên bản phần mềm, gắn nhãn phát hành (release tagging) và dọn dẹp kho lưu trữ.<br>  + Đối soát sơ đồ kiến trúc hạ tầng với tài nguyên đã triển khai thực tế trên môi trường AWS.<br>- **Thực hành:**<br>  + Thực hiện khóa mã nguồn chính thức (Code Freeze) trên nhánh main của kho lưu trữ GitHub (`v1.0.0`).<br>  + Dọn dẹp các tệp cấu hình thử nghiệm, tối ưu mã nguồn và kiểm tra các liên kết tài liệu trên trang web báo cáo. | 09/07/2026 | 09/07/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Chỉnh sửa Hoàn thiện Báo cáo, Đóng gói Tài liệu & Nộp bài Chính thức**<br>- **Kiến thức:**<br>  + Quy chuẩn trình bày và định dạng báo cáo kỹ thuật / báo cáo thực tập tốt nghiệp.<br>  + Rà soát danh mục các sản phẩm bàn giao (deliverables) theo yêu cầu của chương trình.<br>- **Thực hành:**<br>  + Rà soát lỗi chính tả, chuẩn hóa định dạng bìa, mục lục và cấu trúc các file báo cáo.<br>  + Đóng gói toàn bộ hồ sơ (mã nguồn, sơ đồ kiến trúc, link video demo, file báo cáo) và thực hiện nộp bài chính thức qua cổng thông tin. | 10/07/2026 | 10/07/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 12:

#### Thứ Hai (06/07/2026):
* Thực hiện thành công đợt tổng duyệt toàn hệ thống ứng dụng Wakan trên môi trường AWS Production thực tế.
* Xác minh tính thông suốt của toàn bộ hành trình dữ liệu từ phân phối giao diện (S3/CloudFront), xác thực người dùng (Cognito) đến xử lý backend (Lambda/DynamoDB).
* Xác nhận độ trễ phản hồi dưới 1 giây cho các yêu cầu lịch trình đã có trong Cache và không phát sinh bất kỳ lỗi hệ thống nào trên CloudWatch Logs.

#### Thứ Ba (07/07/2026):
* Hoàn thành việc quay và dựng video demo sản phẩm chính thức giới thiệu ứng dụng Trợ lý du lịch Wakan tạo lịch trình bằng AI.
* Ghi lại hình ảnh đối chiếu song song thể hiện AWS WAF chặn đứng các đợt tấn công giả lập và AWS Secrets Manager cấp mã token dynamic an toàn.
* Xuất bản video demo và tích hợp trực tiếp liên kết xem video vào kho lưu trữ tài liệu dự án.

#### Thứ Tư (08/07/2026):
* Hoàn thiện bộ tài liệu báo cáo kỹ thuật chuyên sâu tập trung vào Kiến trúc Đám mây Serverless, Bảo mật Thông tin Đa lớp và Quản trị Chi phí FinOps.
* Nổi bật tính tuân thủ khung chuẩn AWS Well-Architected Framework, phân tích chi tiết IAM Execution Roles đặc quyền tối thiểu, WAF Rate Limits và hệ thống giám sát CloudWatch.
* Đưa vào các sơ đồ minh họa trực quan luồng di chuyển dữ liệu, cơ chế phân tách hệ thống và báo cáo kiểm soát ngân sách.

#### Thứ Năm (09/07/2026):
* Thực hiện khóa mã nguồn chính thức (Code Freeze) trên kho lưu trữ GitHub và gắn nhãn phiên bản hoàn chỉnh.
* Dọn dẹp các file rác phát sinh trong quá trình thử nghiệm, chuẩn hóa cấu trúc thư mục dự án và kiểm tra tính hợp lệ của mã nguồn.
* Đảm bảo toàn bộ tài liệu kỹ thuật và nhật ký công việc (Worklogs) trên website báo cáo Netlify đã được đồng bộ hoàn toàn.

#### Thứ Sáu (10/07/2026):
* Hoàn tất đợt rà soát cuối cùng về mặt định dạng, văn phong và chỉn chu hình thức của tất cả các tệp báo cáo thực tập.
* Đóng gói trọn bộ hồ sơ sản phẩm bàn giao bao gồm: mã nguồn dự án, sơ đồ kiến trúc hạ tầng, liên kết video demo sản phẩm và file báo cáo chính thức.
* Thực hiện nộp bài báo cáo dự án Wakan thành công qua cổng tiếp nhận đúng thời hạn, chính thức khép lại kỳ thực tập 12 tuần chương trình First Cloud AI Journey.