---
title : "Các bước chuẩn bị"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.2. </b> "
---

#### Cài đặt và cấu hình AWS CLI

Toàn bộ phần Auth & User Profile (Lê Hoài Huân) này thực hiện bằng AWS CLI v2. Kiểm tra xem đã cài chưa:

```bash
aws --version
```

![aws --version](/images/5-Workshop/5.2-Prerequiste/01-version.png)

Cấu hình credentials và region mặc định (đúng region `ap-southeast-1` mà PeriodIQ đang chạy):

```bash
aws configure
```

Kiểm tra lại credentials đã hoạt động chưa:

```bash
aws sts get-caller-identity
```

![aws sts get-caller-identity](/images/5-Workshop/5.2-Prerequiste/02-identity.png)

> **CLI Note:** `aws sts get-caller-identity` là cách nhanh nhất để xác nhận CLI đã xác thực đúng và lấy Account ID trước khi chạy bất kỳ lệnh nào khác.

#### Quyền IAM cần thiết

Với vai trò Lê Hoài Huân, IAM user của tôi cần quyền cho đúng các dịch vụ tôi phụ trách: `cognito-idp`, `wafv2`, `cloudfront`, cùng quyền `iam` cơ bản để cấu hình role cho Auth. Với tài khoản cá nhân/sandbox, cách đơn giản nhất là gắn policy managed `AdministratorAccess` của AWS.

> **CLI Note:** mọi bước trên trang này - kiểm tra version, configure, kiểm tra identity - đều là lệnh CLI. Các mục 5.3.1-5.3.4 tiếp theo cũng vậy: mọi thao tác đều qua CLI, console chỉ được mở sau đó để đối chiếu bằng chứng, không phải để thao tác thay CLI.
