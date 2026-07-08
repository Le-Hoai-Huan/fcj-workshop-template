---
title: "Worklog Tuần 6: ECS & Tự động hóa CI/CD (CodePipeline)"
date: 2026-07-07
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Mục tiêu tuần 6:
- Triển khai các ứng dụng container sử dụng Amazon Elastic Container Service (ECS) và Fargate.
- Xây dựng quy trình tích hợp và triển khai liên tục (CI/CD) trên AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu |
| --- | --------- | ------------ | --------------- | -------------- |
| 2 | - Họp nhóm kickoff dự án PeriodIQ, phân tích kiến trúc AWS Serverless và nhận nhiệm vụ.<br>- Tìm hiểu Amazon Elastic Container Service (ECS)<br>  + Khái niệm Cluster, Task Definition, Service<br>  + ECS on EC2 vs AWS Fargate | 25/05/2026 | 25/05/2026 | <https://000016.awsstudygroup.com/vi/> |
| 3 | - Tạo Task Definition sử dụng image từ ECR<br>- Khởi tạo ECS Cluster với AWS Fargate<br>- Cấu hình ECS Service tích hợp với Application Load Balancer | 26/05/2026 | 26/05/2026 | <https://000016.awsstudygroup.com/vi/> |
| 4 | - Giám sát metrics của container trên CloudWatch<br>- Kiểm thử tính năng rolling update của ECS Service<br>- Dọn dẹp các tài nguyên ECS | 27/05/2026 | 27/05/2026 | <https://000016.awsstudygroup.com/vi/> |
| 5 | - Giới thiệu CI/CD trên AWS<br>  + AWS CodeCommit (Source Control)<br>  + AWS CodeBuild (Build & Test)<br>  + AWS CodeDeploy (Deployment) | 28/05/2026 | 28/05/2026 | <https://000017.awsstudygroup.com/vi/> |
| 6 | - Thiết lập repository trên CodeCommit<br>- Viết `buildspec.yml` cho CodeBuild<br>- Tích hợp các dịch vụ thành một AWS CodePipeline hoàn chỉnh | 29/05/2026 | 29/05/2026 | <https://000017.awsstudygroup.com/vi/> |
| 7 | - Kích hoạt pipeline tự động bằng lệnh git push<br>- Phân tích và sửa lỗi build qua log CodeBuild<br>- Viết tài liệu quy trình CI/CD | 30/05/2026 | 30/05/2026 | <https://000017.awsstudygroup.com/vi/> |


### Kết quả đạt được tuần 6:
- Triển khai thành công ECS Service với tính sẵn sàng cao sử dụng AWS Fargate và ALB.
- Liên kết thành công CodeCommit, CodeBuild và CodeDeploy thành một CodePipeline tự động hoàn toàn.
- Kích hoạt thành công tính năng tự động cập nhật (rolling update) khi push code.
