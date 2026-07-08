---
title: "Week 6 Worklog: ECS & CI/CD Pipelines"
date: 2026-07-07
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Week 6 Objectives:
- Deploy containerized applications using Amazon Elastic Container Service (ECS) and Fargate.
- Implement Continuous Integration and Continuous Deployment (CI/CD) pipelines on AWS.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 | - Project kickoff meeting, analyze AWS Serverless architecture and assign tasks.<br>- Learn Amazon Elastic Container Service (ECS)<br>  + Cluster, Task Definition, Service concepts<br>  + ECS on EC2 vs AWS Fargate | 25/05/2026 | 25/05/2026 | <https://000016.awsstudygroup.com> |
| 3 | - Create Task Definitions using images from ECR<br>- Initialize an ECS Cluster with AWS Fargate<br>- Configure ECS Service integrated with Application Load Balancer | 26/05/2026 | 26/05/2026 | <https://000016.awsstudygroup.com> |
| 4 | - Monitor container metrics in CloudWatch<br>- Test rolling updates for the ECS Service<br>- Clean up ECS resources | 27/05/2026 | 27/05/2026 | <https://000016.awsstudygroup.com> |
| 5 | - Introduction to CI/CD on AWS<br>  + AWS CodeCommit (Source Control)<br>  + AWS CodeBuild (Build & Test)<br>  + AWS CodeDeploy (Deployment) | 28/05/2026 | 28/05/2026 | <https://000017.awsstudygroup.com> |
| 6 | - Setup repositories on CodeCommit<br>- Write `buildspec.yml` for CodeBuild<br>- Integrate services into a complete AWS CodePipeline | 29/05/2026 | 29/05/2026 | <https://000017.awsstudygroup.com> |
| 7 | - Trigger pipeline executions via git push<br>- Troubleshoot build failures in CodeBuild logs<br>- Document the CI/CD workflow | 30/05/2026 | 30/05/2026 | <https://000017.awsstudygroup.com> |


### Week 6 Achievements:
- Deployed a highly available ECS Service using AWS Fargate and ALB.
- Connected CodeCommit, CodeBuild, and CodeDeploy into a fully automated CodePipeline.
- Successfully triggered rolling updates via git pushes.
