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
| 1 | - Create a CloudFront distribution `periodiq-frontend-dev` 📄 for the project. Test the endpoint. | 08/06/2026 | 08/06/2026 | Screenshot AWS Console - CloudFront |
| 2 | - Define WAF Web ACLs and managed rulesets. Add AWS Managed Rules for common vulnerabilities. | 09/06/2026 | 09/06/2026 | Screenshot AWS Console - WAF Rules |
| 3 | - Implement rate limiting rules to prevent DDoS on the authentication endpoints. | 10/06/2026 | 10/06/2026 | WAF Block Evidence |
| 4 | - Attach WAF to the CloudFront distribution and API Gateway. Verify response headers. | 11/06/2026 | 11/06/2026 | CloudFront / WAF Headers |
| 5 | - Simulate malicious traffic to test WAF blocking. Monitor WAF metrics and logs in CloudWatch. | 12/06/2026 | 12/06/2026 | CloudWatch Metrics |
| 6 | - Generate test user accounts and verify CloudWatch logs contain `POST /api/users/login` 📄 with HTTP 200. | 13/06/2026 | 13/06/2026 | CloudWatch Log Evidence |


### Week 11 Achievements:
- Created a CloudFront distribution integrated with AWS WAF Web ACLs.
- Verified WAF rules effectively blocked malicious requests.
- Collected screenshots and CloudWatch logs mapping the entire Auth flow.
