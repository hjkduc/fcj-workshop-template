---
title: "Nhật ký Tuần 6"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu Tuần 6:
* Xây dựng kiến thức nền tảng về Data Lake, Quản trị dữ liệu (Data Governance) và quy trình Phân tích dữ liệu trên AWS.
* Học cách truy vấn dữ liệu Serverless bằng Amazon Athena và trực quan hóa báo cáo thông minh (BI) với Amazon QuickSight.
* Đi sâu vào quản trị CSDL quan hệ nâng cao với Amazon Aurora PostgreSQL và làm quen với quy trình Học máy (Machine Learning) trên Amazon SageMaker.

### Công việc triển khai trong tuần:

| Thứ | Nội dung công việc | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | --- | --- | --- | --- |
| 2 | **Chủ đề: Nền tảng AWS Data Lake & Thiết kế Kiến trúc Data Lake**<br>- **Kiến thức:**<br>  + So sánh Data Lake vs Data Warehouse: Sự khác biệt, tách biệt giữa lưu trữ và tính toán, dữ liệu cấu trúc vs phi cấu trúc.<br>  + AWS Lake Formation: Quản trị dữ liệu tập trung, phân quyền chi tiết (cấp hàng/cột) và tạo Danh mục dữ liệu (Data Catalog).<br>- **Thực hành:**<br>  + Nạp các tập dữ liệu thô vào các tầng lưu trữ tối ưu trên Amazon S3.<br>  + Cấu hình phân quyền trên AWS Lake Formation và đăng ký S3 path vào AWS Glue Data Catalog. | 25/05/2026 | 25/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 3 | **Chủ đề: Tổng quan dịch vụ Data Analytics & Báo cáo thông minh (BI) với QuickSight**<br>- **Kiến thức:**<br>  + Hệ sinh thái AWS Analytics: Amazon Kinesis (xử lý dữ liệu thời gian thực), EMR (Big Data), Redshift (Kho dữ liệu).<br>  + Amazon QuickSight: Công cụ BI điện toán đám mây, bộ nhớ đệm SPICE, bảng điều khiển tương tác và phân tích bằng AI/ML.<br>- **Thực hành:**<br>  + Kết nối Amazon QuickSight với nguồn dữ liệu Athena/S3 qua bộ nhớ đệm SPICE.<br>  + Thiết kế và xuất bản bảng điều khiển phân tích kinh doanh (Dashboard) tương tác trực quan. | 26/05/2026 | 26/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 4 | **Chủ đề: Data Engineering Immersion Day & Phân tích Serverless với Amazon Athena**<br>- **Kiến thức:**<br>  + Truy vấn Serverless: Amazon Athena, Presto SQL engine, mô hình chi phí tính theo dung lượng truy vấn.<br>  + Tối ưu hóa hiệu năng & chi phí: Định dạng lưu trữ dạng cột (Apache Parquet / ORC), nén dữ liệu (Snappy), kỹ thuật phân vùng dữ liệu (Partitioning).<br>- **Thực hành:**<br>  + Chuyển đổi tệp dữ liệu thô JSON/CSV sang định dạng Parquet bằng AWS Glue ETL job.<br>  + Thực hiện truy vấn SQL phân tích trên Amazon Athena và đo lường lượng chi phí tiết kiệm được sau khi phân vùng. | 27/05/2026 | 27/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 5 | **Chủ đề: PostgreSQL nâng cao trên AWS - Phần 1 & 2 (Amazon Aurora PostgreSQL)**<br>- **Kiến thức:**<br>  + Kiến trúc Amazon Aurora: CSDL quan hệ Cloud-native, sao lưu dữ liệu phân tán 6 bản sao, Serverless v2, Read Replicas.<br>  + Tối ưu hóa hiệu năng CSDL: Amazon RDS Performance Insights, phân tích Query Execution Plan, plugin pgvector cho tác vụ AI.<br>- **Thực hành:**<br>  + Khởi tạo cụm CSDL Amazon Aurora PostgreSQL Serverless v2 có khả năng tự động co giãn sức chứa.<br>  + Phân tích điểm nghẽn hiệu năng và tối ưu các câu lệnh SQL chậm bằng RDS Performance Insights. | 28/05/2026 | 28/05/2026 | <https://cloudjourney.awsstudygroup.com/> |
| 6 | **Chủ đề: Khái niệm Học máy & Huấn luyện mô hình với Amazon SageMaker**<br>- **Kiến thức:**<br>  + Vòng đời dự án Machine Learning (End-to-End): Chuẩn bị dữ liệu, xây dựng, huấn luyện, tinh chỉnh, triển khai và giám sát mô hình.<br>  + Bộ công cụ Amazon SageMaker: SageMaker Studio, các thuật toán dựng sẵn (XGBoost), Managed Spot Training, Inference Endpoints.<br>- **Thực hành:**<br>  + Tiền xử lý và làm sạch dữ liệu mẫu trong môi trường Jupyter Notebook trên Amazon SageMaker Studio.<br>  + Huấn luyện mô hình phân loại XGBoost và triển khai lên một real-time SageMaker Inference Endpoint. | 29/05/2026 | 29/05/2026 | <https://cloudjourney.awsstudygroup.com/> |

---

### Kết quả đạt được trong Tuần 6:

#### Thứ Hai (25/05/2026):
* Hiểu rõ sự khác biệt về mặt kiến trúc giữa Data Warehouse truyền thống và Data Lake hiện đại trên Amazon S3.
* Cấu hình chính sách bảo mật và phân quyền truy cập dữ liệu chi tiết ở cấp độ hàng và cột bằng AWS Lake Formation.
* Đăng ký tập dữ liệu thô vào AWS Glue Data Catalog để tạo dựng kho quản lý danh mục dữ liệu tập trung.

#### Thứ Ba (26/05/2026):
* Tổng quan toàn bộ hệ sinh thái xử lý và phân tích dữ liệu lớn trên AWS (Kinesis, EMR, Redshift, QuickSight).
* Kết nối thành công Amazon QuickSight với các nguồn dữ liệu trên Cloud và tận dụng bộ nhớ đệm SPICE để tăng tốc độ truy xuất.
* Xây dựng bảng điều khiển Báo cáo thông minh (BI Dashboard) tích hợp các chỉ số KPI và biểu đồ trực quan.

#### Thứ Tư (27/05/2026):
* Làm chủ kỹ thuật Data Engineering Serverless bằng cách sử dụng Amazon Athena để truy vấn SQL trực tiếp trên dữ liệu S3.
* Tối ưu hóa hiệu năng và giảm chi phí truy vấn bằng cách chuyển đổi dữ liệu thô sang định dạng cột Apache Parquet qua AWS Glue.
* Tối ưu lượng dữ liệu quét (data scanned) thông qua việc phân vùng dữ liệu (Partitioning) hợp lý.

#### Thứ Năm (28/05/2026):
* Nâng cao kỹ năng quản trị CSDL với kiến trúc doanh nghiệp của Amazon Aurora PostgreSQL Serverless v2.
* Đánh giá cơ chế tự động nhân bản lưu trữ trên nhiều Availability Zone và khả năng mở rộng đọc (read-scaling) tức thì của Aurora.
* Thao tác trên RDS Performance Insights để phát hiện các câu lệnh SQL tốn tài nguyên và tinh chỉnh chỉ mục CSDL.

#### Thứ Sáu (29/05/2026):
* Nắm vững toàn bộ vòng đời phát triển một mô hình Học máy (Machine Learning Lifecycle) chuẩn hóa trên AWS.
* Sử dụng Amazon SageMaker Studio để chuẩn bị dữ liệu, xây dựng pipeline đặc trưng và huấn luyện mô hình bằng thuật toán XGBoost.
* Triển khai thành công mô hình đã huấn luyện lên một SageMaker Real-time Inference Endpoint phục vụ dự đoán qua API.