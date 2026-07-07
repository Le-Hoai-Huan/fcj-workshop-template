---
title: "Worklog Tuần 10: Thiết kế Kiến trúc & Thiết lập Cognito"
date: 2026-07-07
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Mục tiêu tuần 10:
- Khởi tạo Cognito User Pool và cấu hình luồng xác thực.
- Phát triển các Lambda trigger và API Gateway endpoint cho User Profile.
- Đảm bảo tính liên kết giữa API Gateway, Lambda và DynamoDB.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 1 | - Khởi tạo Cognito User Pool qua Console. Cấu hình chính sách mật khẩu và cài đặt MFA. | 01/06/2026 | 01/06/2026 | Screenshot AWS Console - Cognito |
| 2 | - Cấu hình App Clients và domain cho Cognito. Kiểm thử hosted UI cho đăng ký và đăng nhập. | 02/06/2026 | 02/06/2026 | Screenshot AWS Console - App Client |
| 3 | - Phát triển hàm Lambda `periodiq-auth-post-confirmation` 📄. Thêm IAM role để Lambda ghi vào DynamoDB. | 03/06/2026 | 03/06/2026 | Screenshot AWS Console - Lambda |
| 4 | - Thiết lập API Gateway route `ANY /api/users/profile` 📄. Tạo các resource và method tương ứng. | 04/06/2026 | 04/06/2026 | Screenshot AWS Console - API Gateway |
| 5 | - Tích hợp API Gateway với Cognito Authorizer. Đảm bảo các endpoint được bảo vệ bằng JWT token. | 05/06/2026 | 05/06/2026 | JWT Integration Docs |
| 6 | - Kiểm thử luồng đăng ký và đăng nhập bằng Postman. Xác minh token được truyền đúng. | 06/06/2026 | 06/06/2026 | Postman Evidence |


### Kết quả đạt được tuần 10:
- Triển khai Cognito User Pool với các chính sách mật khẩu tùy chỉnh và App Clients.
- Kiểm thử thành công các API Gateway route được tích hợp với Lambda và DynamoDB.
- Giả lập thành công luồng đăng ký và đăng nhập của người dùng.
