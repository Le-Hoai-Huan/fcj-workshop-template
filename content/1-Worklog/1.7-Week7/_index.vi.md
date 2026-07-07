---
title: "Worklog Tuần 7: Bảo mật hệ thống & Kết nối VPC Peering"
date: 2026-07-07
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Mục tiêu tuần 7:
- Quản lý thế trận bảo mật và đánh giá tính tuân thủ bằng AWS Security Hub.
- Kết nối các mạng VPC bị cô lập bằng VPC Peering.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Tìm hiểu AWS Security Hub và quản lý thế trận bảo mật<br>  + Kích hoạt Security Hub<br>  + Các tiêu chuẩn bảo mật (AWS Foundational Security Best Practices, CIS) | 01/06/2026 | 01/06/2026 | <https://000018.awsstudygroup.com/vi/> |
| 3 | - Phân tích các phát hiện (Findings) từ Security Hub<br>- Liên kết với AWS Config để đánh giá tính tuân thủ<br>- Khắc phục các rủi ro bảo mật cơ bản được cảnh báo | 02/06/2026 | 02/06/2026 | <https://000018.awsstudygroup.com/vi/> |
| 4 | - Tự động hóa quá trình khắc phục bằng EventBridge<br>- Xuất báo cáo tính tuân thủ (compliance report)<br>- Viết tài liệu tổng quan bảo mật | 03/06/2026 | 03/06/2026 | <https://000018.awsstudygroup.com/vi/> |
| 5 | - Khái niệm kết nối mạng VPC Peering<br>  + Nguyên lý hoạt động và giới hạn (không bắt cầu - no transitive routing)<br>  + Kịch bản ứng dụng VPC Peering | 04/06/2026 | 04/06/2026 | <https://000019.awsstudygroup.com/vi/> |
| 6 | - Khởi tạo kết nối VPC Peering giữa 2 VPC<br>- Chấp nhận (Accept) yêu cầu peering<br>- Cấu hình Route Table và Security Group để 2 VPC giao tiếp | 05/06/2026 | 05/06/2026 | <https://000019.awsstudygroup.com/vi/> |
| 7 | - Kiểm thử kết nối mạng chéo giữa các VPC (ping, SSH)<br>- Khắc phục các sự cố liên quan đến định tuyến<br>- Xóa bỏ cấu hình peering sau khi hoàn thành | 06/06/2026 | 06/06/2026 | <https://000019.awsstudygroup.com/vi/> |


### Kết quả đạt được tuần 7:
- Phân tích và khắc phục thành công các lỗ hổng bảo mật được phát hiện bởi Security Hub.
- Thiết lập và định tuyến thành công lưu lượng qua kết nối VPC Peering.
- Xác minh thành công khả năng giao tiếp chéo giữa các VPC bằng ICMP và SSH.
