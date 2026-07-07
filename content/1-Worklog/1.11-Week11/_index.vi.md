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
| 2 | - Khởi tạo WebACL trên AWS WAF (scope CLOUDFRONT tại us-east-1), bật AWS Managed Rules (chặn SQLi, XSS, Bot). | 29/06/2026 | 29/06/2026 |  |
| 3 | - Cấu hình rule giới hạn tốc độ (Rate limiting) để chống DDoS, gắn WAF vào CloudFront distribution qua thuộc tính WebACLId. | 30/06/2026 | 30/06/2026 |  |
| 4 | - Setup CloudFront: Origin S3 (Frontend) và Origin API Gateway (Backend), định tuyến behavior `/api/*`. | 01/07/2026 | 01/07/2026 |  |
| 5 | - Lập trình React Frontend: Xây dựng UI trang Login, Register, Forgot Password và User Profile. | 02/07/2026 | 02/07/2026 |  |
| 6 | - Tích hợp Frontend: Viết Axios interceptor tự động đính kèm JWT Bearer token và logic auto refresh token. | 03/07/2026 | 03/07/2026 |  |
| 7 | - Kiểm thử End-to-End luồng đăng ký -> nhận OTP -> đăng nhập -> tạo User Profile trên giao diện Web. | 04/07/2026 | 04/07/2026 |  |


### Kết quả đạt được tuần 11:
- Tạo thành công CloudFront distribution được tích hợp với AWS WAF Web ACLs.
- Xác minh các quy tắc WAF chặn hiệu quả các request độc hại.
- Thu thập đầy đủ ảnh chụp màn hình và log CloudWatch phản ánh toàn bộ luồng Xác thực.
