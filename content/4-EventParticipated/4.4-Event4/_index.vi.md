---
title: "Event 4"
date: 2026-06-06
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---


# Bài thu hoạch “FCAJ Community Day”

**Thời gian:** 09:00, ngày 06/06/2026

### Mục Đích Của Sự Kiện

- Giới thiệu các dự án thật do thành viên tự xây dựng, trải dài từ bảo mật, networking cho game đến generative AI trên AWS
- Chia sẻ những hành trình sự nghiệp thực tế — từ IT Helpdesk lên Senior Sysadmin, và từ sinh viên trở thành kỹ sư cloud/bảo mật
- Giới thiệu công nghệ nền tảng (Docker) và kiến trúc AI ứng dụng (GraphRAG) qua các phần trình bày thực chiến
- Củng cố các nguyên tắc làm việc nhóm giúp dự án kỹ thuật và hackathon thực sự "ra được sản phẩm"

### Danh Sách Diễn Giả

- **Le Hoang Gia Dai** – Team AWS G3 - *AWS WAF + Machine Learning NIDS for Cyber Attack Detection*
- **Bao Huynh** – Junior Cloud Native Developer, Endava Vietnam / Founder, ITea Lab - *Docker – A Containerization Technology*
- **Tran Trung Vinh** – System Administrator, Central Retail Group - *From IT Helpdesk to Senior Sysadmin*
- **Nguyen Quoc Bao** – *Multiplayer in the Cloud: Connecting Godot Clients with AWS WebSockets*
- **Truong Huy Phuoc** – *The Art of Effective Teamwork*
- **Viet Phat** – Sinh viên ngành AI, Swinburne University of Technology - *GraphRAG: Building GraphRAG Applications with Amazon Bedrock and Amazon Neptune*

### Nội Dung Nổi Bật

#### AWS WAF + Machine Learning NIDS for Cyber Attack Detection

- **AWS WAF** bảo vệ CloudFront, ALB, API Gateway và Cognito trước các exploit phổ biến (SQL Injection, XSS, bot traffic, brute force) bằng detection dựa trên rule — hiệu quả với các mẫu tấn công đã biết, nhưng yếu trước tấn công zero-day và các biến thể mới/lai.
- Để vượt qua giới hạn của rule tĩnh, dự án xây dựng một **NIDS dựa trên Machine Learning** huấn luyện trên bộ dữ liệu CSE-CIC-IDS2018 (Đại học New Brunswick): gộp các file CSV thô, làm sạch giá trị không hợp lệ/NaN/vô cực, loại bỏ cột không cần thiết, và cân bằng lại các lớp tấn công trước khi huấn luyện mô hình **LightGBM**.
- Kiến trúc đầy đủ trên AWS: VPC, EC2, ALB, WAF, S3, Kinesis Data Firehose, Lambda, Security Hub, GuardDuty, Inspector, SNS, IAM, Config, CloudWatch — đối chiếu dự đoán từ NIDS ML với sự kiện WAF trên một dashboard thời gian thực để phát hiện tấn công tốt hơn so với chỉ dùng một trong hai.
- Bài học: chất lượng dữ liệu và cân bằng lớp quyết định hiệu năng ML; chỉ dựa vào signature-based là chưa đủ; NIDS dựa trên ML bổ trợ hiệu quả cho AWS WAF chứ không thay thế hoàn toàn.

#### Docker – A Containerization Technology

- Máy ảo (VM) mỗi cái đều mang theo một hệ điều hành riêng, tốn nhiều CPU/bộ nhớ/lưu trữ hơn và cần update riêng lẻ — quá nặng cho nhiều ứng dụng nhỏ.
- **Containerization** đóng gói một ứng dụng cùng mọi thứ nó cần vào một gói duy nhất, chạy nhất quán ở bất kỳ đâu, dùng chung kernel của host OS — khiến container nhẹ hơn nhiều so với VM.
- Ý tưởng cốt lõi của **Docker**: *build once, run anywhere*. Mỗi instruction trong Dockerfile tạo ra một layer của image; Docker tái sử dụng các layer không đổi từ cache và chỉ rebuild layer thay đổi (cùng mọi layer phía sau nó).
- Các use case phổ biến: pipeline CI/CD, kiến trúc microservices, môi trường dev/test, ứng dụng cloud-native, và hiện đại hóa ứng dụng cũ (legacy modernization).

#### From IT Helpdesk to Senior Sysadmin

- Một hành trình sự nghiệp không xuất phát từ bằng cấp trường top: bắt đầu ở IT Helpdesk, các kỹ năng có thể chuyển hóa cốt lõi là xử lý sự cố dưới áp lực, giao tiếp với end-user, và tư duy giải quyết vấn đề — bước ngoặt đến từ việc tự học Linux, networking, và tự xây dựng lab thực hành.
- Cuộc sống của một sysadmin không chỉ xoay quanh server: provisioning, quản lý network, vá lỗi, capacity planning. Bài học chính — tự động hóa việc lặp lại, ghi tài liệu cấu hình/runbook, giám sát *trước khi* sự cố xảy ra, và **không bao giờ test trên production**.
- Bước chuyển từ Sysadmin sang Cloud/DevOps là một sự thay đổi tư duy, không chỉ là đổi công cụ: từ scaling thủ công on-premise → hạ tầng AWS co giãn, pay-as-you-go → Infrastructure as Code với Terraform → văn hóa DevOps với CI/CD, Docker, và phối hợp chặt chẽ hơn với dev.
- Lời khuyên phỏng vấn và sự nghiệp: dự án thật và kinh nghiệm thực tế quan trọng hơn chỉ có chứng chỉ; các lỗi thường gặp là học quá nhiều thứ cùng lúc, thực hành chưa đủ, và sợ thất bại — hãy đào sâu 1-2 kỹ năng cốt lõi trước, và nhớ rằng **xuất phát điểm không quan trọng, quan trọng là bạn tiếp tục đi**.

#### Multiplayer in the Cloud: Godot + AWS WebSockets

- Chọn đúng mô hình networking rất quan trọng: **UDP/ENet** cho game FPS/đua xe cần độ trễ thấp, **WebSocket** cho nhu cầu turn-based/lobby/chat cần độ tin cậy và full-duplex, còn **HTTP polling** phù hợp cho nhu cầu đơn giản, stateless như login hay leaderboard.
- Kiến trúc xây dựng cho một demo matchmaking turn-based: Godot client → **API Gateway WebSocket** (route `$connect`/`$disconnect`/`$default`) → **Lambda** (Node.js) → **DynamoDB** (dùng `connectionId` làm partition key, lưu status/opponent/choice) → CloudWatch để logging.
- Về phía client, `WebSocketPeer` của Godot xử lý kết nối; việc poll() mỗi frame điều khiển game loop, gửi/nhận message JSON để tiến qua các bước matchmaking, chọn nước đi, và phân giải kết quả.
- Các thách thức thực tế xuất hiện: **kết nối "chết"** (`GoneException`) khi player đã disconnect nhưng vẫn còn trong DynamoDB, **chi phí Scan của DynamoDB** tăng theo số lượng player, và tính **stateless** của Lambda buộc phải round-trip tới DynamoDB ở mọi request.
- Hướng tiếp theo: cách tiếp cận WebSocket + Lambda hiện tại phù hợp cho game turn-based, trong khi **AWS GameLift** phù hợp hơn cho game real-time tần suất cao cần trạng thái in-memory bền vững và dedicated server.

#### The Art of Effective Teamwork

- Bốn quy tắc vàng cho một team hiệu quả: **mục tiêu rõ ràng và được chia sẻ chung**, **đúng người đúng việc**, **giao tiếp cởi mở và lắng nghe chủ động**, và **trách nhiệm cá nhân**.
- Các công cụ số hỗ trợ làm việc nhóm: Trello và ClickUp để theo dõi công việc, Google Workspace và Slack để cộng tác/giao tiếp, và Discord để phối hợp nhóm theo thời gian thực.

#### GraphRAG: Building GraphRAG Applications with Amazon Bedrock and Amazon Neptune

- **RAG** tăng cường LLM tại thời điểm chạy bằng cách truy xuất các đoạn văn liên quan từ knowledge base và đưa vào prompt — nhưng RAG thông thường gặp khó với các **câu hỏi multi-hop** (ví dụ: "công ty được acquire bởi công ty do Jeff Bezos sáng lập có trụ sở ở đâu?") vì không thể suy luận qua chuỗi quan hệ.
- **GraphRAG** giải quyết vấn đề này bằng cách lưu trữ quan hệ tường minh dưới dạng cạnh (edge) của đồ thị và dùng graph traversal để **suy luận multi-hop** qua nhiều entity và tài liệu.
- Hai hướng triển khai được so sánh: **hướng fully managed** dùng Amazon Bedrock Knowledge Bases (chunking, trích xuất entity, tạo embedding) kết hợp Amazon Neptune Analytics (lưu trữ đồ thị, phát hiện quan hệ); và **hướng custom** dùng pipeline xử lý LlamaIndex kết hợp Amazon Neptune với truy vấn Cypher trực tiếp cho traversal multi-hop.

### Những Gì Học Được

#### Phòng thủ nhiều lớp hiệu quả hơn bất kỳ control đơn lẻ nào

- Công cụ dựa trên rule như AWS WAF và công cụ học/hành vi như NIDS dựa trên ML bắt được các loại tấn công khác nhau — kết hợp tín hiệu từ cả hai hiệu quả hơn chỉ dùng một

#### Chọn đúng công cụ cho đúng ràng buộc

- Containerization vs. virtualization, WebSocket vs. UDP vs. HTTP polling, GraphRAG managed vs. custom — bài học lặp lại là chọn cách tiếp cận dựa trên ràng buộc thực tế (mức tài nguyên, độ trễ, khả năng kiểm soát) thay vì mặc định theo thứ quen thuộc

#### Phát triển sự nghiệp thưởng cho chiều sâu và thực hành thật, hơn là bằng cấp

- Cả hành trình sysadmin lẫn kỹ sư bảo mật đều có chung một điểm: lab thực hành, dự án thật, và đào sâu vài nền tảng cốt lõi quan trọng hơn xuất thân hay chỉ có chứng chỉ

#### Hệ thống phân tán thường lỗi ở phần "rìa" (state cũ, chi phí khi scale)

- Cả kiến trúc NIDS đa luồng lẫn WebSocket multiplayer đều gặp cùng một loại vấn đề — state tồn tại lâu hơn kết nối, hoặc chi phí scan tăng theo dữ liệu — một lời nhắc phải thiết kế cho việc dọn dẹp và khả năng scale ngay từ đầu

#### Kết quả kỹ thuật vẫn phụ thuộc vào nền tảng làm việc nhóm

- Không điều nào ở trên có ý nghĩa nếu thiếu mục tiêu rõ ràng, đúng người đúng vai trò, và giao tiếp trung thực — các quy tắc "mềm" về teamwork chính là nền tảng quyết định công việc kỹ thuật có thực sự hoàn thành hay không

### Ứng Dụng Vào Công Việc

- **Phòng thủ nhiều lớp**: kết hợp công cụ dựa trên rule (WAF) với phát hiện dựa trên bất thường/ML khi threat model có khả năng gặp mẫu tấn công mới
- **Mặc định dùng container** cho service mới, trừ khi có lý do cụ thể cần cô lập toàn phần kiểu VM
- **Chọn mô hình networking theo đúng use case** — đừng mặc định dùng WebSocket hay UDP thô, hãy kiểm tra yêu cầu về độ trễ và độ tin cậy trước
- **Đầu tư vào 1-2 kỹ năng chuyên sâu** và một project thật trong portfolio trước khi dàn trải công sức vào nhiều chứng chỉ
- **Lên kế hoạch dọn dẹp connection/state một cách tường minh** trong bất kỳ kiến trúc serverless + WebSocket hay pub/sub nào, thay vì phát hiện ra vấn đề khi đã lên production
- **Đánh giá GraphRAG** (managed hoặc custom) cho bất kỳ use case RAG nào cần suy luận qua nhiều quan hệ, không chỉ truy xuất một tài liệu đơn lẻ
- **Rà lại 4 quy tắc teamwork** (mục tiêu chung, đúng người đúng vai trò, giao tiếp cởi mở, trách nhiệm) khi bắt đầu bất kỳ dự án hoặc team hackathon mới nào

### Trải nghiệm trong event

Tham gia phiên này của **“FCAJ Community Day”** là một dịp tốt để thấy việc "build trên AWS" có thể đa dạng đến thế nào — từ bảo mật, networking cho game, đến generative AI và cả những nền tảng sysadmin cơ bản. Một số trải nghiệm nổi bật:

#### Nhìn bảo mật như một bài toán nhiều lớp, luôn tiến hóa
- Dự án WAF + ML NIDS của Le Hoang Gia Dai là ví dụ cụ thể về việc kết hợp phòng thủ dựa trên rule và phòng thủ dựa trên học máy, và là lời nhắc rằng **không có control đơn lẻ nào là đủ** trước các tấn công liên tục tiến hóa.

#### Có được nền tảng rõ ràng, thực tế về container
- Phần trình bày Docker của Bao Huynh khiến sự đánh đổi giữa VM và container trở nên cụ thể, củng cố lý do container đã trở thành khối xây dựng mặc định cho triển khai hiện đại.

#### Nghe một câu chuyện sự nghiệp không bắt đầu từ một CV "hoàn hảo"
- Hành trình của Tran Trung Vinh từ IT Helpdesk lên Senior Sysadmin (rồi sang Cloud/DevOps) là lời nhắc thực tế rằng thực hành đều đặn có thể quan trọng hơn xuất phát điểm.

#### Chứng kiến hạ tầng multiplayer thời gian thực được xây dựng và giải thích từ đầu đến cuối
- Demo Godot + AWS WebSocket của Nguyen Quoc Bao kết nối code game phía client với thiết kế backend serverless theo cách khiến các đánh đổi (và cả các lỗi thường gặp) trở nên rất cụ thể.

#### Được nhắc rằng dự án hoàn thành vẫn là một môn thể thao đồng đội
- Phần chia sẻ về teamwork của Truong Huy Phuoc là một lời nhắc hữu ích: không phiên kỹ thuật nào ở trên có thể hoàn thành nếu thiếu mục tiêu rõ ràng, đúng vai trò, và giao tiếp trung thực trong team.

#### Có cái nhìn thực tế về điểm RAG "gãy" — và cách GraphRAG khắc phục
- Phần trình bày GraphRAG của Viet Phat biến một nhận định mơ hồ "RAG không đủ cho câu hỏi phức tạp" thành cụ thể, chỉ rõ những câu hỏi multi-hop nào khiến RAG thường thất bại, và cách Bedrock + Neptune (managed hoặc custom) có thể lấp đầy khoảng trống đó.

#### Bài học rút ra
- Kết hợp các kỹ thuật bổ trợ nhau (rule + ML, container + orchestration, RAG + graph) luôn tốt hơn chỉ dựa vào một cách tiếp cận.
- Hệ thống phân tán trong thực tế (backend WebSocket, pipeline ML) thường lỗi ở phần rìa — state cũ và chi phí khi scale — nên cần thiết kế cho việc dọn dẹp ngay từ đầu.
- Kết quả sự nghiệp và dự án đều phụ thuộc vào nền tảng cơ bản và teamwork không kém gì công nghệ cụ thể được chọn.

#### Một số hình ảnh khi tham gia sự kiện

![FCAJ Community Day - Event 4 photo 1](/images/4-Event/4.4-Event4/image5.png)
![FCAJ Community Day - Event 4 photo 2](/images/4-Event/4.4-Event4/image6.png)


> Tổng thể, phiên FCAJ Community Day này đã kết nối bảo mật mạng, containerization, phát triển sự nghiệp, networking multiplayer thời gian thực, teamwork, và generative AI ứng dụng thành một bức tranh chung: các khối xây dựng kỹ thuật vững chắc chỉ thực sự trở thành dự án hoàn thiện và bền vững khi đi kèm nền tảng cơ bản và cách làm việc nhóm đúng đắn.
