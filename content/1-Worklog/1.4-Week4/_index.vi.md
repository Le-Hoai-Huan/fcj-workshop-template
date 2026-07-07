---
title: "Worklog Tuần 4: DNS, CLI & Sao lưu dữ liệu"
date: 2026-07-07
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:
- Cấu hình tên miền và các chính sách định tuyến sử dụng Amazon Route 53.
- Thành thạo công cụ AWS CLI để quản lý tài nguyên bằng dòng lệnh.
- Triển khai các chính sách bảo vệ dữ liệu tập trung bằng AWS Backup.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Tìm hiểu dịch vụ DNS Amazon Route 53<br>  + Đăng ký tên miền (Domain registration)<br>  + Khái niệm Public và Private Hosted Zone | 11/05/2026 | 11/05/2026 | <https://000010.awsstudygroup.com/vi/> |
| 3 | - Tạo các bản ghi DNS (A, CNAME, ALIAS, TXT)<br>- Tìm hiểu và cấu hình Routing Policies (Simple, Weighted, Failover)<br>- Kiểm tra phân giải tên miền | 12/05/2026 | 12/05/2026 | <https://000010.awsstudygroup.com/vi/> |
| 4 | - Cài đặt và cấu hình AWS Command Line Interface (CLI)<br>- Cấu hình Access Key và Secret Key qua `aws configure`<br>- Tìm hiểu các profile trong AWS CLI | 13/05/2026 | 13/05/2026 | <https://000011.awsstudygroup.com/vi/> |
| 5 | - Sử dụng CLI tương tác với S3 (s3api, s3 sync, cp)<br>- Thao tác quản lý EC2 thông qua giao diện dòng lệnh<br>- Viết shell script tự động hóa tác vụ cơ bản | 14/05/2026 | 14/05/2026 | <https://000011.awsstudygroup.com/vi/> |
| 6 | - Tìm hiểu dịch vụ AWS Backup tập trung<br>  + Backup Plans, Backup Vaults<br>  + Lifecycle policies (chuyển sang cold storage) | 15/05/2026 | 15/05/2026 | <https://000013.awsstudygroup.com/vi/> |
| 7 | - Khởi tạo Backup Plan để sao lưu định kỳ EBS volume<br>- Gán tags cho tài nguyên để tự động backup<br>- Thực hành khôi phục (Restore) dữ liệu từ điểm sao lưu | 16/05/2026 | 16/05/2026 | <https://000013.awsstudygroup.com/vi/> |


### Kết quả đạt được tuần 4:
- Định tuyến thành công lưu lượng tên miền bằng các chính sách của Route 53.
- Tự động hóa các tác vụ AWS cơ bản bằng script CLI và quản lý profile.
- Tạo thành công các kế hoạch sao lưu tự động và khôi phục dữ liệu từ EBS snapshot.
