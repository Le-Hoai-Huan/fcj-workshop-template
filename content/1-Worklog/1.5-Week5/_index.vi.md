---
title: "Worklog Tuần 5: VM Import & Cơ bản về Container (Docker)"
date: 2026-07-07
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Mục tiêu tuần 5:
- Chuyển đổi và di chuyển máy ảo on-premises lên AWS bằng VM Import/Export.
- Tìm hiểu các khái niệm container hóa và thực hành build Docker images.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Khái niệm AWS VM Import/Export<br>- Chuẩn bị môi trường và các công cụ đóng gói máy ảo (OVA, VMDK)<br>- Cấu hình IAM Role và S3 bucket chứa file ảnh (image) | 18/05/2026 | 18/05/2026 | <https://000014.awsstudygroup.com/vi/> |
| 3 | - Sử dụng AWS CLI để import VM vào EC2 AMI<br>- Theo dõi quá trình import/export<br>- Khởi chạy EC2 instance từ AMI vừa import | 19/05/2026 | 19/05/2026 | <https://000014.awsstudygroup.com/vi/> |
| 4 | - Kiểm tra lại các cấu hình hệ thống sau khi import<br>- Dọn dẹp các file tạm trên S3<br>- Viết tài liệu quy trình migration | 20/05/2026 | 20/05/2026 | <https://000014.awsstudygroup.com/vi/> |
| 5 | - Tìm hiểu nền tảng container hóa với Docker<br>  + Kiến trúc Image, Container, Docker Engine<br>  + Viết Dockerfile cơ bản (FROM, RUN, CMD) | 21/05/2026 | 21/05/2026 | <https://000015.awsstudygroup.com/vi/> |
| 6 | - Build Docker image cho một ứng dụng web (Node.js/Python)<br>- Chạy và quản lý container (docker run, ps, stop)<br>- Khởi tạo Amazon ECR và push image lên ECR | 22/05/2026 | 22/05/2026 | <https://000015.awsstudygroup.com/vi/> |
| 7 | - Kiểm thử kết nối mạng và volume của container<br>- Tối ưu hóa Dockerfile để giảm dung lượng image<br>- Viết tài liệu hướng dẫn container hóa | 23/05/2026 | 23/05/2026 | <https://000015.awsstudygroup.com/vi/> |


### Kết quả đạt được tuần 5:
- Import thành công một image máy ảo bên ngoài và khởi chạy thành EC2 instance.
- Viết Dockerfile tối ưu và quản lý các container nội bộ hiệu quả.
- Đẩy thành công các image ứng dụng tùy chỉnh lên kho lưu trữ Amazon ECR.
