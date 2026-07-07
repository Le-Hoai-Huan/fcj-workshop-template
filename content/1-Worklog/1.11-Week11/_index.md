---
title: "Week 11 Worklog: Edge Security & WAF Integration"
date: 2026-07-07
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives:
- Secure the API and frontend infrastructure using AWS WAF and CloudFront.
- Monitor authentication events and logs via CloudWatch.
- Collect evidence for the workshop report.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2 | - Provision WebACL on AWS WAF (CLOUDFRONT scope in us-east-1), enable AWS Managed Rules (SQLi, XSS, Bot protection). | 29/06/2026 | 29/06/2026 |  |
| 3 | - Configure Rate limiting rules to prevent DDoS, attach WAF to CloudFront distribution via WebACLId. | 30/06/2026 | 30/06/2026 |  |
| 4 | - Setup CloudFront: S3 Origin (Frontend) and API Gateway Origin (Backend), configure `/api/*` behavior. | 01/07/2026 | 01/07/2026 |  |
| 5 | - React Frontend Development: Build UI for Login, Register, Forgot Password, and User Profile pages. | 02/07/2026 | 02/07/2026 |  |
| 6 | - Frontend Integration: Write Axios interceptor for automatic JWT Bearer token injection and refresh logic. | 03/07/2026 | 03/07/2026 |  |
| 7 | - Conduct E2E testing for the registration -> OTP -> login -> create profile flow on the Web UI. | 04/07/2026 | 04/07/2026 |  |


### Week 11 Achievements:
- Created a CloudFront distribution integrated with AWS WAF Web ACLs.
- Verified WAF rules effectively blocked malicious requests.
- Collected screenshots and CloudWatch logs mapping the entire Auth flow.
