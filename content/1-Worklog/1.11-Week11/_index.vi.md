---
title: "Worklog Tuần 11: Bảo mật Biên & Tích hợp WAF"
date: 2026-07-07
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Mục tiêu tuần 11:
- Bảo mật API và hạ tầng frontend bằng AWS WAF và CloudFront.
- Giám sát các sự kiện xác thực và log thông qua CloudWatch.
- Thu thập minh chứng (evidence) cho báo cáo workshop.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 1 | - Tạo CloudFront distribution `periodiq-frontend-dev` 📄 cho dự án. Kiểm thử endpoint. | 08/06/2026 | 08/06/2026 | Screenshot AWS Console - CloudFront |
| 2 | - Định nghĩa WAF Web ACLs và các tập quy tắc quản lý. Thêm AWS Managed Rules cho các lỗ hổng phổ biến. | 09/06/2026 | 09/06/2026 | Screenshot AWS Console - WAF Rules |
| 3 | - Cài đặt quy tắc giới hạn tốc độ (rate limit) để chống DDoS trên các endpoint xác thực. | 10/06/2026 | 10/06/2026 | WAF Block Evidence |
| 4 | - Đính kèm WAF vào CloudFront distribution và API Gateway. Xác minh các header phản hồi. | 11/06/2026 | 11/06/2026 | CloudFront / WAF Headers |
| 5 | - Giả lập truy cập độc hại để kiểm thử tính năng chặn của WAF. Giám sát các metric WAF trong CloudWatch. | 12/06/2026 | 12/06/2026 | CloudWatch Metrics |
| 6 | - Sinh tài khoản test và kiểm tra CloudWatch logs có `POST /api/users/login` 📄 với HTTP 200. | 13/06/2026 | 13/06/2026 | CloudWatch Log Evidence |


### Kết quả đạt được tuần 11:
- Tạo thành công CloudFront distribution được tích hợp với AWS WAF Web ACLs.
- Xác minh các quy tắc WAF chặn hiệu quả các request độc hại.
- Thu thập đầy đủ ảnh chụp màn hình và log CloudWatch phản ánh toàn bộ luồng Xác thực.
