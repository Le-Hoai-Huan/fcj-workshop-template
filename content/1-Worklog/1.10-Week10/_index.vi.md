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
| 2 | - Khởi tạo Amazon Cognito User Pool, cấu hình App Client, thiết lập User Groups (Users, Admins). | 22/06/2026 | 22/06/2026 |  |
| 3 | - Setup luồng gửi mã OTP qua email cho xác minh tài khoản khi đăng ký mới. | 23/06/2026 | 23/06/2026 |  |
| 4 | - Lập trình .NET Backend: Cấu hình JWT Bearer Authentication trong `Program.cs` để validate token từ Cognito. | 24/06/2026 | 24/06/2026 |  |
| 5 | - Lập trình .NET Backend: Tạo `UserProfilesController` (CRUD profile, map Cognito sub ID vào bảng DynamoDB). | 25/06/2026 | 25/06/2026 |  |
| 6 | - Cấu hình Middleware `[Authorize]` để phân quyền truy cập cho User và role Admins. | 26/06/2026 | 26/06/2026 |  |
| 7 | - Kiểm thử Backend APIs (đăng nhập, lấy profile) bằng Swagger/Postman với token thực sinh ra từ Cognito. | 27/06/2026 | 27/06/2026 |  |


### Kết quả đạt được tuần 10:
- Triển khai Cognito User Pool với các chính sách mật khẩu tùy chỉnh và App Clients.
- Kiểm thử thành công các API Gateway route được tích hợp với Lambda và DynamoDB.
- Giả lập thành công luồng đăng ký và đăng nhập của người dùng.
