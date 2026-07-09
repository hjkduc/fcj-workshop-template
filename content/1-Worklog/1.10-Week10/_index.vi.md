---
title: "Worklog Tuần 10"
date: 2026-06-22
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:
* Thiết lập hệ sinh thái giám sát và cảnh báo lỗi toàn diện.
* Kiểm soát chi phí hạ tầng thông qua cảnh báo ngân sách.
* Chạy thử toàn bộ hệ thống (End-to-end test) và khắc phục lỗi.

### Các công việc đã hoàn thành:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái |
| --- | --- | --- | --- | --- |
| 2 | - Test End-to-End lần đầu toàn hệ thống | 22/06/2026 | 22/06/2026 | Hoàn thành |
| 3 | - Cấu hình tập trung CloudWatch Logs | 23/06/2026 | 23/06/2026 | Hoàn thành |
| 4 | - Cài đặt CloudWatch Alarms theo dõi ngưỡng lỗi | 24/06/2026 | 24/06/2026 | Hoàn thành |
| 5 | - Dựng AWS Budget alert cảnh báo % credit tiêu thụ | 25/06/2026 | 25/06/2026 | Hoàn thành |
| 6 | - Họp fix bug liên phòng ban | 26/06/2026 | 26/06/2026 | Hoàn thành |

### Kết quả đạt được:
* **Khả năng quan sát (Observability):** Hệ thống đã có khả năng lưu log tập trung và tự động gửi cảnh báo qua CloudWatch Alarms khi có bất thường.
* **Kiểm soát chi phí:** Đảm bảo dự án không bị vượt ngân sách credit thông qua việc thiết lập AWS Budget alert.