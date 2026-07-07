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
| 2 | - Provision Amazon Cognito User Pool, configure App Client, and setup User Groups (Users, Admins). | 22/06/2026 | 22/06/2026 |  |
| 3 | - Setup email OTP verification flow for new user registrations. | 23/06/2026 | 23/06/2026 |  |
| 4 | - .NET Backend Development: Configure JWT Bearer Authentication in `Program.cs` to validate Cognito tokens. | 24/06/2026 | 24/06/2026 |  |
| 5 | - .NET Backend Development: Create `UserProfilesController` (Profile CRUD, mapping Cognito sub ID to DynamoDB). | 25/06/2026 | 25/06/2026 |  |
| 6 | - Configure `[Authorize]` Middleware to enforce role-based access control (RBAC) for Users and Admins. | 26/06/2026 | 26/06/2026 |  |
| 7 | - Test Backend APIs using Swagger/Postman with real JWT tokens generated from Cognito. | 27/06/2026 | 27/06/2026 |  |


### Week 10 Achievements:
- Deployed Cognito User Pool with custom password policies and App Clients.
- Tested API Gateway routes integrated with Lambda and DynamoDB.
- Successfully simulated user registration and login flows.
