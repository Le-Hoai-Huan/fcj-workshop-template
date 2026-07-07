---
title: "Week 10 Worklog: Architecture Design & Cognito Setup"
date: 2026-07-07
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives:
- Provision the Cognito User Pool and configure authentication workflows.
- Develop Lambda triggers and API Gateway endpoints for User Profile.
- Ensure integration between API Gateway, Lambda, and DynamoDB.

### Tasks to be carried out this week:
| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 1 | - Provision the Cognito User Pool via Console. Configure password policies and MFA settings. | 01/06/2026 | 01/06/2026 | Screenshot AWS Console - Cognito |
| 2 | - Configure App Clients and domain for Cognito. Test the hosted UI for sign-up and sign-in. | 02/06/2026 | 02/06/2026 | Screenshot AWS Console - App Client |
| 3 | - Develop Lambda function `periodiq-auth-post-confirmation` 📄. Add IAM role for Lambda to write to DynamoDB. | 03/06/2026 | 03/06/2026 | Screenshot AWS Console - Lambda |
| 4 | - Set up API Gateway route `ANY /api/users/profile` 📄. Create resources and methods. | 04/06/2026 | 04/06/2026 | Screenshot AWS Console - API Gateway |
| 5 | - Integrate API Gateway with Cognito Authorizer. Ensure endpoints are protected by JWT tokens. | 05/06/2026 | 05/06/2026 | JWT Integration Docs |
| 6 | - Test registration and login flows using Postman. Verify tokens are passed correctly. | 06/06/2026 | 06/06/2026 | Postman Evidence |


### Week 10 Achievements:
- Deployed Cognito User Pool with custom password policies and App Clients.
- Tested API Gateway routes integrated with Lambda and DynamoDB.
- Successfully simulated user registration and login flows.
