---
title: "Event 2"
date: 2026-05-23
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---


# Bài thu hoạch “FCAJ Community Day”

**Thời gian:** 09:00, ngày 23/05/2026

### Mục Đích Của Sự Kiện

- Kết nối các AWS community builder, kỹ sư và sinh viên để chia sẻ kinh nghiệm thực chiến về AI, kiến trúc cloud và xây dựng ứng dụng hiện đại
- Khám phá khía cạnh thực tế khi làm việc với LLM — từ những điểm bất ổn định cho đến context engineering
- Giới thiệu các case study thực tế từ production và hackathon của cộng đồng
- Đào sâu về Amazon CloudFront như nền tảng cho chi phí, bảo mật và hiệu năng ở edge

### Danh Sách Diễn Giả

- **Duc Dao** – Solution Architect, Cloud Kinetics — *Non-Determinism of “Deterministic” LLM Settings*
- **Vy Lam** – Senior Business Systems Analyst, VPBank — *Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring*
- **Pham Nguyen Hai Anh** – AWS Community Builder, G-AsiaPacific Vietnam — *Friendly AI Assistant w/ Amazon Quick*
- **Nguyen Tuan Thinh** – DevOps Engineer, First Cloud AI Journey — *From Edge to Origin: CloudFront as Your Foundation*
- **Tinh Truong** – Platform Engineer, GoTymeX — *Context Is Everything*
- **Team VIB** – Đội thi LotusHacks 2026 — *UTMorpho: Building UTMorpho from Idea to Reality*

### Nội Dung Nổi Bật

#### Tính không ổn định của "Deterministic" LLM Settings

- `temperature=0` được cho là đảm bảo output tái lặp được, nhưng nghiên cứu (Atil et al., 2024) chỉ ra rằng **không có model nào cho output nhất quán** trên toàn bộ task được kiểm thử — độ chính xác chênh lệch tới 15%, khoảng cách best-to-worst lên tới 70%
- Nguyên nhân gốc: **phép toán floating-point không có tính kết hợp (non-associative) trên GPU** cộng với **inference batching** — kết quả tính toán của request phụ thuộc vào những request khác trong cùng batch
- Giải pháp giảm thiểu: chạy nhiều lần rồi lấy đa số (majority voting), dùng structured/constrained output, tự host model để kiểm soát toàn bộ, và thiết kế logic downstream coi output LLM là **xác suất, không phải tất định**
- Mẹo thực tế: `temp=0.1` thường an toàn hơn `temp=0` vì tránh được tình trạng model bị lặp vòng lặp (repetitive loop)

#### Enterprise-Grade Multi-Agent System — Credit Scoring cho Startup

- Mô hình chấm điểm tín dụng truyền thống thất bại với startup vì được xây dựng dựa trên báo cáo tài chính 3+ năm và định dạng chuẩn hóa — không phù hợp với startup chỉ có 6-18 tháng hoạt động, tăng trưởng nóng và dữ liệu phi cấu trúc
- Một **single agent** gặp khó khi cần chuyên môn đa lĩnh vực, mục tiêu xung đột và khả năng audit — vẫn chạy được nhưng cho ra quyết định thiếu tin cậy với các quyết định rủi ro cao
- Giải pháp đề xuất là **virtual credit committee**: nhiều agent chuyên biệt (Financial, Market, Team, Risk, Compliance) phối hợp dưới một Manager agent để ra điểm số đồng thuận, xếp hạng rủi ro, mức độ tin cậy và audit trail đầy đủ
- Tư duy enterprise-grade xoay quanh 6 trụ cột: **security, data governance, network, operations, human factors, compliance** — kết quả đo được cho thấy xử lý nhanh hơn 95% và ROI 3 năm đạt 200–300%

#### Friendly AI Assistant với Amazon Quick

- Người dùng doanh nghiệp thường xuyên phải làm các tác vụ lặp lại, tốn thời gian để tổng hợp và phân tích thông tin từ nhiều nguồn khác nhau
- **Amazon Quick Suite** mang lại trải nghiệm thống nhất, bảo mật, kết hợp dữ liệu công ty, kiến thức chung, hơn 40 data connector và khả năng agentic (automation flow, dashboard, chat, research) trong một lớp quản trị có guardrail và access control
- Demo thực tế: một PM assistant tự động tạo biên bản họp (MoM), gửi email cho stakeholder và lên lịch cuộc họp tiếp theo

#### From Edge to Origin: CloudFront as Your Foundation

- Mô hình tính phí CDN theo usage rất khó dự đoán — hóa đơn có thể chỉ $0.03 nhưng cũng có thể tăng vọt lên $100K vì traffic viral hoặc bị tấn công
- Các **gói CDN + bảo mật giá cố định** mới (ra mắt tháng 11/2025) gộp CloudFront, WAF, chống DDoS, Route 53 và logging CloudWatch vào một mức phí hàng tháng dễ dự đoán
- CloudFront cải thiện đáng kể về **chi phí** (nén dữ liệu, miễn phí data transfer từ AWS origin), **bảo mật** (TLS 1.3/mTLS, Origin Shield/OAC/VPC origin để ẩn origin, signed URL), **độ bền vững** (multi-layer caching, origin failover, graceful degradation) và **hiệu năng** (HTTP/3, kết nối backbone bền vững, edge compute)

#### Context Is Everything

- Phần lớn câu trả lời AI gây thất vọng đến từ **context kém, không phải model kém** — AI không thể tự suy ra mục tiêu hay đọc được suy nghĩ của bạn
- Các lỗi thường gặp: nhồi nhét mọi thứ vào một đoạn chat (vấn đề "internet puller"), nhắc lại những gì model đã biết, và không nêu rõ mục tiêu/ràng buộc/tiêu chí thành công
- Cách dùng AI đang tiến hóa từ **prompt** đơn lẻ → **context** có căn cứ → **memory** lâu dài (store → retrieve → generate → learn), minh họa qua case study "Second AI Brain"
- Một framework đơn giản trước khi hỏi AI: **Goal, thông tin liên quan, ràng buộc, tiêu chí thành công**

#### UTMorpho — Xây Dựng Sản Phẩm Trong 36 Giờ (LotusHacks 2026)

- Một hành trình nhìn lại của cả team, từ lúc "đầu óc trống rỗng" khi đăng ký đến khi hoàn thành UTMorpho trong 36 giờ hackathon
- Các thách thức chính: AI sinh output quá đà (overgeneration), giới hạn token, và kiệt sức gần giờ pitch — được giải quyết nhờ tập trung chỉnh sửa và đồng bộ team tốt hơn
- Bài học: **sự bực bội thực sự tạo ra ý tưởng thực sự**, nhưng nhiều ý tưởng hơn không đồng nghĩa với ý tưởng tốt hơn — sức bền và sự đồng bộ của team quan trọng không kém kỹ thuật

### Những Gì Học Được

#### Độ tin cậy của AI là bài toán thiết kế, không chỉ là bài toán model

- Các setting tất định như `temp=0` chỉ giảm chứ không loại bỏ hoàn toàn tính ngẫu nhiên — cần thiết kế hệ thống chấp nhận được sự biến thiên này
- Kiến trúc multi-agent vượt trội hơn single agent cho các quyết định cần audit, rủi ro cao và đa lĩnh vực

#### Context Engineering đang trở thành kỹ năng cốt lõi

- Context tốt hơn — chứ không phải nhiều hơn — mới là yếu tố quyết định chất lượng output AI
- Việc chuyển dịch từ prompting sang context system rồi đến memory dài hạn là khoảng kỹ năng tiếp theo cần lấp đầy

#### Nền tảng hạ tầng vẫn quan trọng

- Khả năng edge của CloudFront (bảo mật, chi phí dự đoán được, hiệu năng) vẫn là nền tảng ngay cả trong một stack thiên về AI
- Tư duy enterprise-grade (security, governance, compliance) cần được thiết kế ngay từ đầu, không phải gắn thêm về sau

### Ứng Dụng Vào Công Việc

- **Coi output LLM là xác suất**: thêm majority-voting hoặc ràng buộc structured-output cho bất kỳ pipeline nào đang dựa vào `temp=0` để đảm bảo tính nhất quán
- **Thử nghiệm mô hình multi-agent** cho các workflow hiện đang dồn hết vào một agent quá tải
- **Áp dụng framework 4 phần** (goal, thông tin liên quan, ràng buộc, tiêu chí thành công) trước khi viết prompt cho công việc thực tế
- **Đánh giá các gói giá cố định của CloudFront** cho các dự án có traffic khó dự đoán để tránh rủi ro hóa đơn tăng đột biến
- **Thử Amazon Quick Suite** cho các workflow lặp lại trong công việc (ghi biên bản họp, cập nhật stakeholder, lên lịch)

### Trải nghiệm trong event

Tham gia **“FCAJ Community Day”** là cơ hội tuyệt vời để thấy cách các mảng khác nhau trong cộng đồng AWS — từ kỹ sư doanh nghiệp đến các bạn làm hackathon — đang áp dụng AI và nền tảng cloud theo những cách rất thực tế và khác biệt. Một số trải nghiệm nổi bật:

#### Học hỏi từ chính người thực hành trong cộng đồng, không chỉ từ tài liệu chính thức
- Các diễn giả chia sẻ **những phát hiện trực tiếp**, như nghiên cứu về tính tất định của LLM, thay vì chỉ nói theo hướng marketing.
- Case study credit scoring cho startup cho thấy cách **thiết kế multi-agent** giải quyết bài toán audit thực tế trong ngành có quản lý chặt như ngân hàng.

#### Kết nối giữa hạ tầng và các vấn đề AI
- Phiên về CloudFront là lời nhắc hữu ích rằng **nền tảng edge và networking** vẫn cực kỳ quan trọng, ngay cả trong lộ trình tập trung vào AI.
- Phần nói về context engineering giúp nhìn nhận lại prompting như một **vấn đề trải nghiệm sản phẩm**, chứ không chỉ là mẹo dùng từ ngữ.

#### Nhìn thấy khía cạnh "người xây dựng" của cộng đồng
- Phần chia sẻ của Team VIB về LotusHacks là một góc nhìn rất thật về cảm giác build sản phẩm trong 36 giờ — bao gồm cả những thất bại, không chỉ phần demo.
- Điều này càng khẳng định **sự đồng bộ của team và sức bền** quan trọng không kém kỹ năng kỹ thuật thuần túy khi chạy đua với thời gian.

#### Bài học rút ra
- Độ tin cậy của hệ thống AI cần được **thiết kế chủ động**, không thể chỉ dựa vào một setting temperature.
- Thiết kế context tốt và thiết kế hạ tầng tốt đều theo cùng một nguyên tắc: **cung cấp cho hệ thống đúng những gì nó cần, không thừa không thiếu**.
- Các sự kiện cộng đồng như thế này mang lại những bài học thực tế mà tài liệu chính thức khó có thể truyền tải hết.

#### Một số hình ảnh khi tham gia sự kiện

![FCAJ Community Day - Event 2 photo 1](/images/4-Event/4.2-Event2/image2.png)

> Tổng thể, sự kiện đã kết nối các mảnh ghép về độ tin cậy của AI, thiết kế hệ thống agentic, context engineering và nền tảng hạ tầng cloud thành một bức tranh nhất quán — đồng thời khẳng định rằng các nguyên tắc kỹ thuật vững chắc vẫn quan trọng không kém trong thời đại AI như trước đây.
