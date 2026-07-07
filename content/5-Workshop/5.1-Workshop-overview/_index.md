---
title : "Introduction"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

#### What is PeriodIQ?

PeriodIQ is a serverless application that generates a personalized 4-week gym workout plan for a user based on their fitness level, body weight, training goal, and Personal Records, using a rule-based engine (Volume Filter -> Conflict Resolution -> Progression Builder). The full architecture (16 AWS services across 8 layers) is described in the [Proposal](../../2-proposal/) section.

#### How the team split the work

| Section | Role | AWS Services |
|---|---|---|
| **Lê Hoài Huân (me)** | **Auth & User Profile** | **Amazon Cognito, AWS WAF, Amazon CloudFront** |
| Trần Anh Tài | Rule Engine & Workout Generation | Lambda (API Handler + Rule Engine), Amazon S3 |
| Lê Hữu Duy Hoàng | Progress & Async Notification | Amazon SQS, Lambda Worker, Amazon SNS |
| Chương Tử Luân | Admin Panel & Data | Lambda Admin API, Amazon DynamoDB, API Gateway |
| Phạm Văn Sỹ | CI/CD & Monitoring | AWS CodePipeline, AWS CodeBuild, CloudFormation/SAM, Amazon CloudWatch |

#### Scope of this workshop

This workshop documents **my own role, Lê Hoài Huân**, in detail, focusing on the Authentication and Edge Security layer. The setup involves Amazon Cognito for user management, AWS WAF for application security, and Amazon CloudFront for content delivery. Every command in [section 5.3](../5.3-nguoi1-auth/) is a genuine `aws` CLI call against that real deployment - reading user pools, configuring WAF web ACLs, and setting up CloudFront distributions - with a real terminal screenshot as evidence for each one.

> **CLI Note:** because this workshop documents the live production system rather than a disposable sandbox copy, everything here is **read-only** - `describe-*`, `get-*`, `list-*` - against the real resources. Nothing was deployed, changed, or deleted on the real infrastructure while writing this section (see [Clean up](../5.8-cleanup/) for what that means in practice).
