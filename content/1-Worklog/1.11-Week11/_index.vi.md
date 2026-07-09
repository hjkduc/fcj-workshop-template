---
title: "Worklog Tuần 11"
date: 2026-06-29
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:
* Thực hiện kiểm thử thâm nhập (Pentest) cơ bản để đánh giá bảo mật.
* Rà soát phân quyền IAM và chống rò rỉ dữ liệu nhạy cảm.
* Chốt các điểm cần tối ưu trước thềm demo dự án.

### Các công việc đã hoàn thành:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Trạng thái |
| --- | --- | --- | --- | --- |
| 2 | - Họp tổng duyệt kết quả kiểm thử toàn nhóm | 29/06/2026 | 29/06/2026 | Hoàn thành |
| 3 | - Pentest cơ bản: Thử tấn công qua WAF (XSS, SQLi) | 30/06/2026 | 30/06/2026 | Hoàn thành |
| 4 | - Rà soát và siết chặt các policy IAM thừa quyền | 01/07/2026 | 01/07/2026 | Hoàn thành |
| 5 | - Kiểm tra chống rò rỉ tại Secrets Manager | 02/07/2026 | 02/07/2026 | Hoàn thành |
| 6 | - Vá các lỗ hổng tìm thấy và chốt báo cáo bảo mật | 03/07/2026 | 03/07/2026 | Hoàn thành |

### Kết quả đạt được:
* **Kiểm thử An toàn thông tin:** Xác thực thành công khả năng chặn đứng các cuộc tấn công web của WAF và đảm bảo tuyệt đối an toàn cho API key.
* **Tối ưu Đặc quyền:** Hệ thống IAM đã được "dọn dẹp" và siết chặt ở mức tối đa, sẵn sàng cho môi trường Production thu nhỏ.