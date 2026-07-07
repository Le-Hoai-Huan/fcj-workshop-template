---
title: "Worklog Tuần 8: Transit Gateway & Triển khai kiến trúc nâng cao"
date: 2026-07-07
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Mục tiêu tuần 8:
- Xây dựng cấu trúc mạng hình sao (hub-and-spoke) có khả năng mở rộng bằng AWS Transit Gateway.
- Thiết kế và triển khai một hệ thống WordPress mạnh mẽ, có tính sẵn sàng cao trên AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Tìm hiểu AWS Transit Gateway<br>  + Khắc phục nhược điểm của VPC Peering (mạng hình sao - Hub and Spoke)<br>  + Transit Gateway Attachments | 08/06/2026 | 08/06/2026 | <https://000020.awsstudygroup.com/vi/> |
| 3 | - Khởi tạo Transit Gateway và kết nối 3 VPC<br>- Cấu hình Transit Gateway Route Tables<br>- Kiểm tra kết nối mạng (ping, ssh) xuyên suốt các VPC | 09/06/2026 | 09/06/2026 | <https://000020.awsstudygroup.com/vi/> |
| 4 | - Triển khai các domain định tuyến để cô lập mạng<br>- Giám sát lưu lượng đi qua Transit Gateway<br>- Vẽ sơ đồ kiến trúc mạng hình sao | 10/06/2026 | 10/06/2026 | <https://000020.awsstudygroup.com/vi/> |
| 5 | - Phân tích kiến trúc triển khai WordPress tối ưu trên AWS<br>  + Web tier (EC2 + ASG + ALB)<br>  + Database tier (RDS MySQL)<br>  + Shared storage (EFS) | 11/06/2026 | 11/06/2026 | <https://000021.awsstudygroup.com/vi/> |
| 6 | - Triển khai EFS và mount vào EC2 instances<br>- Cài đặt WordPress, kết nối database và lưu file tĩnh trên EFS<br>- Kiểm thử khả năng chịu lỗi (Failover) và cân bằng tải | 12/06/2026 | 12/06/2026 | <https://000021.awsstudygroup.com/vi/> |
| 7 | - Tích hợp CloudFront trước ALB để tối ưu bộ nhớ đệm<br>- Thực hiện kiểm thử chịu tải (load testing)<br>- Hoàn thiện tài liệu kiến trúc WordPress trên AWS | 13/06/2026 | 13/06/2026 | <https://000021.awsstudygroup.com/vi/> |


### Kết quả đạt được tuần 8:
- Tập trung hóa việc định tuyến mạng cho nhiều VPC thông qua Transit Gateway.
- Triển khai kiến trúc WordPress chuẩn production tích hợp EC2, RDS và EFS.
- Xác thực thành công khả năng chịu lỗi và cân bằng tải của hệ thống.
