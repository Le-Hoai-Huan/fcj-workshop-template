---
title : "Prerequiste"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.2. </b> "
---

#### Install and configure the AWS CLI

This whole Auth & User Profile (Lê Hoài Huân) section is done with the AWS CLI v2. Check that it's installed:

```bash
aws --version
```

![aws --version](/images/5-Workshop/5.2-Prerequiste/01-version.png)

Configure your credentials and default region (the same `ap-southeast-1` PeriodIQ runs in):

```bash
aws configure
```

Verify the credentials are working:

```bash
aws sts get-caller-identity
```

![aws sts get-caller-identity](/images/5-Workshop/5.2-Prerequiste/02-identity.png)

> **CLI Note:** `aws sts get-caller-identity` is the fastest way to confirm the CLI is authenticated correctly and to grab your Account ID before running anything else.

#### Required IAM permissions

For the role of Lê Hoài Huân, my IAM user needs permissions for the exact services I am responsible for: `cognito-idp`, `wafv2`, `cloudfront`, along with standard `iam` access for configuring roles related to Auth. For a personal/sandbox account, the simplest approach is to attach the AWS `AdministratorAccess` managed policy.

> **CLI Note:** every step on this page - checking version, configure, checking identity - is a CLI command. The following sections 5.3.1-5.3.4 are the same: all operations are via CLI, the console is only opened afterwards to verify the evidence, not to act as a substitute for the CLI.
