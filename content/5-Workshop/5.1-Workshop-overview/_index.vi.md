---
title : "Giới thiệu"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

#### PeriodIQ là gì?

PeriodIQ là một ứng dụng serverless sinh giáo án tập gym cá nhân hoá trong 4 tuần dựa trên trình độ, cân nặng, mục tiêu tập luyện và Personal Record của người dùng, thông qua một rule engine (Volume Filter -> Conflict Resolution -> Progression Builder). Toàn bộ kiến trúc (16 dịch vụ AWS trải trên 8 tầng) được mô tả ở phần [Proposal](../../2-proposal/).

#### Team đã chia công việc như thế nào

| Mục | Vai trò | Dịch vụ AWS |
|---|---|---|
| **Lê Hoài Huân (tôi)** | **Auth & User Profile** | **Amazon Cognito, AWS WAF, Amazon CloudFront** |
| Trần Anh Tài | Rule Engine & Sinh giáo án | Lambda (API Handler + Rule Engine), Amazon S3 |
| Lê Hữu Duy Hoàng | Tiến trình & Async Notification | Amazon SQS, Lambda Worker, Amazon SNS |
| Chương Tử Luân | Admin Panel & Data | Lambda Admin API, Amazon DynamoDB, API Gateway |
| Phạm Văn Sỹ | CI/CD & Monitoring | AWS CodePipeline, AWS CodeBuild, CloudFormation/SAM, Amazon CloudWatch |

#### Phạm vi của workshop này

Workshop này ghi lại chi tiết **vai trò của chính tôi, Lê Hoài Huân**, tập trung vào tầng Xác thực và Bảo mật Biên (Auth & Edge Security). Hệ thống bao gồm Amazon Cognito để quản lý người dùng, AWS WAF để bảo mật ứng dụng và Amazon CloudFront để phân phối nội dung. Mọi lệnh ở [mục 5.3](../5.3-nguoi1-auth/) đều là lệnh `aws` CLI gọi trực tiếp trên deployment đó - kiểm tra user pools, cấu hình WAF web ACLs, và thiết lập CloudFront - kèm ảnh chụp terminal làm bằng chứng cho từng bước.

> **CLI Note:** vì workshop này ghi lại hệ thống production đang sống thay vì một bản sao sandbox dùng-rồi-bỏ, mọi thứ ở đây đều **chỉ đọc** - `describe-*`, `get-*`, `list-*`. Không có gì bị deploy, thay đổi, hay xoá trên hạ tầng trong lúc viết phần này (xem [Dọn dẹp tài nguyên](../5.8-cleanup/) để biết điều đó có nghĩa gì trong thực tế).
