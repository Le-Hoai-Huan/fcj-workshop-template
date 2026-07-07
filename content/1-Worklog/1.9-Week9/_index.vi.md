---
title: "Worklog Tuần 9: Nghiên cứu dự án & Thiết kế kiến trúc"
date: 2026-07-07
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Mục tiêu tuần 9:
- Phân tích yêu cầu kiến trúc hệ thống PeriodIQ (thiết kế serverless 7 lớp trên AWS).
- Lên phạm vi công việc cho phân hệ Auth & User Profile.
- Thiết lập quyền truy cập nhóm và môi trường ban đầu.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Họp nhóm kickoff dự án PeriodIQ, phân tích kiến trúc AWS Serverless 7 lớp và nhận nhiệm vụ Người 1 (Auth & User Profile). | 15/06/2026 | 15/06/2026 |  |
| 3 | - Đọc tài liệu thiết kế hệ thống, phân tích luồng xác thực qua Cognito và bảo mật biên với WAF & CloudFront. | 16/06/2026 | 16/06/2026 |  |
| 4 | - Thiết lập tài khoản AWS Sandbox, nghiên cứu thư viện xác thực JWT cho .NET 10 và TanStack Query cho React. | 17/06/2026 | 17/06/2026 |  |
| 5 | - Vẽ sơ đồ kiến trúc chi tiết cho phân hệ Xác thực (Cognito -> CloudFront -> WAF -> .NET API). | 18/06/2026 | 18/06/2026 |  |
| 6 | - Thiết kế schema bảng `UserProfile` trên DynamoDB và chuẩn bị danh sách API endpoints cho hồ sơ người dùng. | 19/06/2026 | 19/06/2026 |  |
| 7 | - Trình bày phương án bảo mật JWT và bảo vệ CloudFront với nhóm, chốt scope công việc. | 20/06/2026 | 20/06/2026 |  |


### Kết quả đạt được tuần 9:
- Hoàn thành việc đọc hiểu tài liệu kỹ thuật và giải thích kiến trúc của dự án.
- Thiết lập quyền truy cập cho nhóm thông qua IAM Groups và Users.
- Chốt danh sách các dịch vụ AWS cho phân tầng Auth được giao.
