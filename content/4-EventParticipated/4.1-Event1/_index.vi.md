---
title: "Event 1"
date: 2026-05-09
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---


# Bài thu hoạch “FCAJ Community Day”

**Thời gian:** 09:00, ngày 09/05/2026

### Mục Đích Của Sự Kiện

- Chia sẻ cách các thói quen, công cụ và phương pháp thời AI đang thay đổi cách developer học tập, viết prompt, onboard và xây dựng phần mềm
- Khám phá các kỹ thuật thực tế để cải thiện chất lượng output của LLM thay vì chỉnh sửa thủ công theo cảm tính
- Bàn về điều thực sự khiến một fresher trở nên "sẵn sàng cho AI" trên thị trường tuyển dụng hiện nay
- Giới thiệu một phương pháp có cấu trúc, dựa trên nhiều agent, để phát triển phần mềm với sự hỗ trợ của AI

### Danh Sách Diễn Giả

- **Huynh Hoang Long** – Admin của FCAJ - *Addicted to learning like you're addicted to Social Media*
- **Nguyen Tuan Thinh** – DevOps/Cloud Engineer - *Automated Prompt Engineering: Enhancing LLM Output Quality*
- **Khang** – Solution Architect - *AI-Ready Freshers*
- **Thao** - Software development - *BMAD Method*

### Nội Dung Nổi Bật

#### Addicted to Learning Like You're Addicted to Social Media

- Mạng xã hội giữ chân người dùng nhờ một vòng lặp đơn giản: **trigger (kích hoạt) → action (hành động) → variable reward (phần thưởng biến thiên) → investment (đầu tư)**. Vòng lặp này hoàn toàn có thể được thiết kế lại để phục vụ việc học thay vì lướt mạng vô định.
- Chỉ dựa vào ý chí là không bền vững — môi trường và vòng phản hồi (feedback loop) quan trọng hơn động lực nhất thời trong ngày.
- Các kỹ thuật thực tế được chia sẻ: trigger hằng ngày (nhắc nhở, streak), hành động học tập nhỏ và lặp lại được, phần thưởng biến thiên (kiến thức mới, thắng lợi nhỏ, được cộng đồng công nhận), và thói quen "đầu tư" như ghi chú hoặc chia sẻ công khai để củng cố vòng lặp.
- Bài học: hãy coi việc học đều đặn là một **bài toán thiết kế thói quen**, không phải bài toán kỷ luật cá nhân.

#### Automated Prompt Engineering: Enhancing LLM Output Quality

- Chỉnh sửa prompt thủ công theo kiểu thử-sai không thể scale, và chỉ một thay đổi nhỏ về cách diễn đạt cũng có thể ảnh hưởng đáng kể đến chất lượng và độ ổn định của output.
- Cách tiếp cận tự động hóa: xác định rõ chỉ số thành công và một tập dữ liệu đánh giá, tạo ra nhiều phiên bản prompt, chấm điểm chúng trên tập dữ liệu đó (kể cả dùng LLM-as-judge để chấm), rồi tiếp tục cải thiện phiên bản tốt nhất.
- Cách này biến prompt engineering thành một **quy trình có thể lặp lại và đo lường được**, thay vì đoán mò, giúp so sánh khách quan giữa các phiên bản prompt trước khi đưa vào production.
- Liên hệ chặt với vấn đề độ tin cậy của LLM đã được nhắc tới ở các buổi khác trong cộng đồng — không thể loại bỏ hoàn toàn sự biến thiên của LLM, nhưng có thể giảm thiểu nó một cách có hệ thống.

#### AI-Ready Freshers

- Sinh viên mới ra trường hiện nay bước vào một thị trường mà các công cụ AI đã đảm nhiệm phần lớn công việc lặp lại, mang tính khuôn mẫu — vì vậy chỉ "biết cách viết prompt" không còn là điểm khác biệt.
- Điều thực sự tạo nên một fresher "AI-ready": **nền tảng vững** (cấu trúc dữ liệu, tư duy hệ thống, khả năng debug), khả năng đánh giá phản biện output của AI thay vì chấp nhận mù quáng, và sự tự tin khi làm việc trong các workflow có AI hỗ trợ (Copilot, Amazon Q Developer, v.v.).
- Lời khuyên thực tế: xây dựng các project trong portfolio kết hợp công cụ AI với kỷ luật kỹ thuật thực sự — testing, version control, code review — thay vì chỉ dựa vào "vibe coding".

#### BMAD Method

- **BMAD (Breakthrough Method for Agile AI-Driven Development)** cấu trúc hóa việc phát triển phần mềm có AI hỗ trợ xoay quanh các vai trò agent chuyên biệt — Analyst, PM, Architect, Scrum Master, Developer, QA — mỗi agent phụ trách một giai đoạn rõ ràng trong quy trình.
- Thay vì dựa vào một AI assistant đa năng làm mọi thứ một cách tùy hứng, BMAD tách biệt rõ **giai đoạn lập kế hoạch** và **giai đoạn thực thi**, với mỗi agent tạo ra các tài liệu có cấu trúc (PRD, tài liệu kiến trúc, story file) được bàn giao gọn gàng cho giai đoạn tiếp theo.
- Lợi ích: giữ cho việc phát triển bằng AI vẫn bám sát agile practices, cải thiện khả năng truy vết (traceability), tính nhất quán và sự đồng bộ giữa các thành viên trong dự án, thay vì phụ thuộc vào một phiên chat dài không có cấu trúc.

### Những Gì Học Được

#### Phát triển bản thân cần thiết kế hệ thống, không chỉ cần ý chí

- Thói quen học tập đều đặn có thể được thiết kế giống như cách các đội sản phẩm thiết kế vòng lặp engagement
- Những hành động nhỏ, lặp lại được, có phản hồi rõ ràng hiệu quả hơn những mục tiêu lớn nhưng khó duy trì

#### Viết prompt và ứng dụng AI cần sự chặt chẽ, không chỉ dựa vào cảm tính

- Chất lượng prompt nên được đo lường và cải thiện có hệ thống, không nên chỉnh theo cảm giác
- "AI-ready" nằm ở khả năng phán đoán và nền tảng vững chắc, không chỉ là biết vài mẹo viết prompt

#### Có cấu trúc luôn tốt hơn dùng AI một cách tùy hứng

- BMAD Method cho thấy việc trao cho các AI agent vai trò và bàn giao rõ ràng tạo ra kết quả nhất quán hơn nhiều so với một assistant không có cấu trúc
- Điều này phản ánh một quy luật lớn hơn: AI phát huy tốt nhất khi nằm trong một quy trình được thiết kế tốt, chứ không phải để thay thế việc có quy trình

### Ứng Dụng Vào Công Việc

- **Thiết kế lại một thói quen học tập cá nhân** theo vòng lặp trigger–action–reward–investment (ví dụ: streak hằng ngày, viết bài chia sẻ công khai)
- **Xây dựng một script đánh giá prompt đơn giản** với tập test nhỏ trước khi chốt prompt dùng trong dự án thực tế
- **Ưu tiên tiêu chí nền tảng vững** khi mentor hoặc đánh giá các bạn junior đang làm việc với công cụ AI
- **Thử áp dụng BMAD Method** cho một dự án nhỏ — tách workflow có AI hỗ trợ thành các vai trò Analyst/PM/Architect/Dev/QA riêng biệt thay vì một phiên chat dài không cấu trúc

### Trải nghiệm trong event

Tham gia **“FCAJ Community Day”** là một trải nghiệm mới mẻ khi nhìn vào khía cạnh con người và quy trình khi làm việc với AI — không chỉ là công cụ, mà còn là thói quen và cấu trúc xung quanh việc sử dụng chúng hiệu quả. Một số trải nghiệm nổi bật:

#### Nhìn lại việc học như một thói quen được thiết kế, không phải bài toán kỷ luật
- Phần chia sẻ của Huynh Hoang Long giúp tôi nhìn nhận việc học đều đặn như thứ có thể **thiết kế được**, mượn chính những vòng lặp khiến mạng xã hội gây nghiện — nhưng hướng vào sự phát triển thay vì sao nhãng.

#### Thấy prompt engineering được đối xử như một bộ môn kỹ thuật thực sự
- Phần trình bày của Nguyen Tuan Thinh cho thấy chất lượng prompt không cần dựa vào đoán mò — nó có thể được đo lường, kiểm thử và cải tiến giống như bất kỳ artifact kỹ thuật nào khác.

#### Nhìn lại ý nghĩa thật sự của "AI-ready" đối với sinh viên mới ra trường
- Phần chia sẻ của Khang là một lời nhắc thực tế hữu ích: kỹ năng viết prompt thôi không đủ để fresher nổi bật — nền tảng vững và khả năng phán đoán phản biện với output của AI mới là yếu tố quyết định.

#### Khám phá một cách làm có cấu trúc để phát triển phần mềm với AI
- Phần giới thiệu **BMAD Method** của Thao là một câu trả lời cụ thể cho vấn đề nhiều người trong chúng ta từng gặp — một phiên chat AI dài, không có cấu trúc sẽ khó mà scale được cho các dự án phần mềm thực tế.

#### Bài học rút ra
- Cả việc học lẫn việc viết prompt đều được hưởng lợi khi ta **coi chúng là hệ thống cần thiết kế**, thay vì chỉ cố gắng nhiều hơn.
- Công cụ AI khuếch đại bất kỳ quy trình nào nó được gắn vào — một quy trình tốt sẽ khiến AI hiệu quả hơn rất nhiều.
- "AI-ready" là một tư duy và bộ kỹ năng, không chỉ đơn thuần là quen với một giao diện chat.

#### Một số hình ảnh khi tham gia sự kiện

![FCAJ Community Day - Event 1 photo 1](/images/4-Event/4.1-Event1/image1.jpg)

> Tổng thể, sự kiện đã kết nối thói quen học tập cá nhân, sự chặt chẽ trong prompt engineering, sự sẵn sàng cho sự nghiệp và phương pháp phát triển AI có cấu trúc thành một chủ đề chung: dùng AI tốt phần lớn nằm ở hệ thống và kỷ luật mà bạn xây dựng xung quanh nó.
