---
title: "Week 8 Worklog: Transit Gateway & Advanced Architectures"
date: 2026-07-07
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives:
- Build scalable hub-and-spoke network topologies using AWS Transit Gateway.
- Architect and deploy a robust, highly available WordPress system on AWS.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 | - Learn AWS Transit Gateway<br>  + Overcoming VPC Peering limitations (Hub and Spoke)<br>  + Transit Gateway Attachments | 08/06/2026 | 08/06/2026 | <https://000020.awsstudygroup.com> |
| 3 | - Initialize Transit Gateway and connect 3 VPCs<br>- Configure Transit Gateway Route Tables<br>- Verify end-to-end connectivity | 09/06/2026 | 09/06/2026 | <https://000020.awsstudygroup.com> |
| 4 | - Implement route domains for isolation<br>- Monitor Transit Gateway traffic<br>- Document the hub-and-spoke architecture | 10/06/2026 | 10/06/2026 | <https://000020.awsstudygroup.com> |
| 5 | - Analyze optimal WordPress deployment architecture on AWS<br>  + Web tier (EC2 + ASG + ALB)<br>  + Database tier (RDS)<br>  + Shared storage (EFS) | 11/06/2026 | 11/06/2026 | <https://000021.awsstudygroup.com> |
| 6 | - Deploy EFS and mount to EC2 instances<br>- Install WordPress, connect to database and store static files on EFS<br>- Test failover capabilities | 12/06/2026 | 12/06/2026 | <https://000021.awsstudygroup.com> |
| 7 | - Configure CloudFront in front of ALB for caching<br>- Perform load testing<br>- Finalize WordPress migration report | 13/06/2026 | 13/06/2026 | <https://000021.awsstudygroup.com> |


### Week 8 Achievements:
- Centralized network routing for multiple VPCs using Transit Gateway.
- Deployed a production-ready WordPress architecture integrating EC2, RDS, and EFS.
- Validated the fault tolerance and load balancing capabilities of the architecture.
