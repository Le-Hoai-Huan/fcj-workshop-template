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
| 1 | - Họp nhóm: xem xét kiến trúc hệ thống PeriodIQ (thiết kế serverless 7 lớp trên AWS) và chia dự án thành 5 nhóm role | 25/05/2026 | 25/05/2026 | Project Repo |
| 2 | - Đọc tài liệu kỹ thuật của dự án (giải thích kiến trúc, hướng dẫn schema DynamoDB) để hiểu toàn bộ hệ thống | 26/05/2026 | 26/05/2026 | Architecture Docs |
| 3 | - Thiết lập quyền truy cập cho nhóm trên tài khoản AWS chung: tạo IAM Group cho mỗi role và IAM User | 27/05/2026 | 27/05/2026 | IAM Console |
| 4 | - Nghiên cứu và chốt danh sách các dịch vụ AWS cho phân tầng được giao (Auth & User Profile). Đọc tài liệu về Cognito, API Gateway | 28/05/2026 | 28/05/2026 | AWS Docs |
| 5 | - Vẽ sơ đồ kiến trúc cho lớp Xác thực. Xác định các điểm tích hợp. | 29/05/2026 | 29/05/2026 | Draw.io Diagram |
| 6 | - Trình bày thiết kế kiến trúc ban đầu với nhóm. Thu thập phản hồi và tinh chỉnh luồng xác thực. | 30/05/2026 | 30/05/2026 | Meeting Notes |


### Kết quả đạt được tuần 9:
- Hoàn thành việc đọc hiểu tài liệu kỹ thuật và giải thích kiến trúc của dự án.
- Thiết lập quyền truy cập cho nhóm thông qua IAM Groups và Users.
- Chốt danh sách các dịch vụ AWS cho phân tầng Auth được giao.
