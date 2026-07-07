---
title: "Worklog Tuần 2: Compute & Database (EC2, RDS, ASG)"
date: 2026-07-07
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:
- Làm quen với nền tảng compute qua việc tạo EC2 instance (cấu hình Security Group, Key Pair).
- Triển khai cơ sở dữ liệu quản lý bằng Amazon RDS với Multi-AZ để đảm bảo tính sẵn sàng cao.
- Tìm hiểu Elastic Load Balancing và cấu hình Auto Scaling Groups để tự động mở rộng.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Tìm hiểu compute core trên AWS (EC2)<br>  + Các loại Instance types và AMI<br>  + Elastic Block Store (EBS) vs Instance store<br>- Khởi tạo EC2 instance (Amazon Linux) | 27/04/2026 | 27/04/2026 | <https://000004.awsstudygroup.com/vi/> |
| 3 | - Cấu hình Security Group (Inbound/Outbound rules)<br>- Tạo và quản lý SSH Key Pair để truy cập instance<br>- Kết nối vào EC2 thông qua SSH và EC2 Instance Connect | 28/04/2026 | 28/04/2026 | <https://000004.awsstudygroup.com/vi/> |
| 4 | - Tìm hiểu dịch vụ cơ sở dữ liệu Amazon RDS<br>  + Hỗ trợ các engine (MySQL, PostgreSQL...)<br>  + Khái niệm Multi-AZ deployment cho High Availability<br>- Khởi tạo một database instance với MySQL | 29/04/2026 | 29/04/2026 | <https://000005.awsstudygroup.com/vi/> |
| 5 | - Cấu hình Security Group cho phép EC2 truy cập RDS<br>- Thiết lập tự động sao lưu (Automated Backups)<br>- Khởi tạo Read Replica để giảm tải truy vấn đọc | 30/04/2026 | 30/04/2026 | <https://000005.awsstudygroup.com/vi/> |
| 6 | - Tìm hiểu Elastic Load Balancing (ELB)<br>  + Application Load Balancer (ALB) vs Network Load Balancer (NLB)<br>  + Cấu hình Target Groups và Health Checks<br>- Tạo Launch Template cho EC2 | 01/05/2026 | 01/05/2026 | <https://000006.awsstudygroup.com/vi/> |
| 7 | - Cấu hình Auto Scaling Group (ASG)<br>- Tích hợp ASG với ALB<br>- Kiểm thử tự động scale (Scale out/in) khi có tải | 02/05/2026 | 02/05/2026 | <https://000006.awsstudygroup.com/vi/> |


### Kết quả đạt được tuần 2:
- Khởi tạo thành công EC2 instance và kết nối bảo mật qua SSH.
- Triển khai hệ thống cơ sở dữ liệu MySQL đảm bảo tính sẵn sàng cao bằng RDS.
- Tích hợp thành công Auto Scaling Group với Application Load Balancer để xử lý thay đổi lưu lượng.
