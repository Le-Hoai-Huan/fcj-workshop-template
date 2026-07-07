---
title: "Worklog Tuần 12: User Profile API & Bàn giao Dự án"
date: 2026-07-07
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Mục tiêu tuần 12:
- Thực hiện kiểm thử toàn trình (E2E) lần cuối cho module Auth & User Profile.
- Tối ưu hóa code, tinh chỉnh quyền IAM và viết tài liệu báo cáo.
- Bàn giao module hoàn thiện cho buổi thuyết trình dự án cuối khóa.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 1 | - Thực hiện kiểm thử toàn trình (E2E) cho luồng Xác thực. Kiểm thử các trường hợp ngoại lệ (sai mật khẩu, hết hạn token). | 15/06/2026 | 15/06/2026 | E2E Test Report |
| 2 | - Sửa các lỗi liên quan đến việc hết hạn và làm mới token. Tối ưu hóa code Lambda để cải thiện hiệu năng. | 16/06/2026 | 16/06/2026 | Git Commits |
| 3 | - Tối ưu hóa các role thực thi IAM (đặc quyền tối thiểu). Xem xét tính tuân thủ trên Security Hub cho tài nguyên Auth. | 17/06/2026 | 17/06/2026 | IAM Policy Review |
| 4 | - Viết tài liệu kỹ thuật cho module Xác thực. Document các API endpoint và payload xác thực. | 18/06/2026 | 18/06/2026 | README.md |
| 5 | - Chuẩn bị slide thuyết trình làm nổi bật kiến trúc xác thực serverless và các tính năng bảo mật. | 19/06/2026 | 19/06/2026 | Presentation Slides |
| 6 | - Thuyết trình và bàn giao dự án cuối khóa. Trình diễn module Xác thực đang hoạt động cho giảng viên. | 20/06/2026 | 20/06/2026 | Final Demo |


### Kết quả đạt được tuần 12:
- Giải quyết toàn bộ các lỗi ngoại lệ trong quá trình kiểm thử E2E.
- Bảo mật các IAM role theo nguyên tắc đặc quyền tối thiểu.
- Bàn giao tài liệu kỹ thuật toàn diện và thuyết trình thành công module Xác thực.
