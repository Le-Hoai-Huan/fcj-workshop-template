---
title: "Event 2"
date: 2026-05-23
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---


# Summary Report: “FCAJ Community Day”

**Date & Time:** 09:00, May 23, 2026
### Event Objectives

- Bring together AWS community builders, engineers, and students to share hands-on experience across AI, cloud architecture, and modern application delivery
- Explore the practical side of building with LLMs — from reliability quirks to context engineering
- Showcase real production and hackathon case studies from community members
- Deep-dive into Amazon CloudFront as a foundation for cost, security, and performance at the edge

### Speakers

- **Duc Dao** – Solution Architect, Cloud Kinetics — *Non-Determinism of “Deterministic” LLM Settings*
- **Vy Lam** – Senior Business Systems Analyst, VPBank — *Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring*
- **Pham Ng Hai Anh** – AWS Community Builder, G-AsiaPacific Vietnam — *Friendly AI Assistant w/ Amazon Quick*
- **Nguyen Tuan Thinh** – DevOps Engineer, First Cloud AI Journey — *From Edge to Origin: CloudFront as Your Foundation*
- **Tinh Truong** – Platform Engineer, GoTymeX — *Context Is Everything*
- **Team VIB** – LotusHacks 2026 finalists — *UTMorpho: Building UTMorpho from Idea to Reality*

### Key Highlights

#### Non-Determinism of “Deterministic” LLM Settings

- `temperature=0` is assumed to guarantee reproducible outputs, but research (Atil et al., 2024) found **zero models delivered consistent outputs** across all tested tasks — accuracy varied up to 15%, and best-to-worst accuracy gaps reached 70%
- Root cause: **non-associative floating-point arithmetic on GPUs** plus **inference batching**, where your request's computation depends on what else is in the batch
- Mitigation strategies: multiple runs + majority voting, structured/constrained outputs, self-hosted models for full control, and designing downstream logic to treat LLM output as **probabilistic, not deterministic**
- Practical tip: `temp=0.1` is often a safer sweet spot than `temp=0` to avoid the model getting stuck in repetitive loops

#### Enterprise-Grade Multi-Agent System — Startup Credit Scoring

- Traditional credit scoring models fail on startups because they're built around 3+ years of financials and standardized reporting — not 6-18 months of hypergrowth and unstructured data
- A **single agent** struggles with multi-domain expertise, conflicting objectives, and auditability — it works, but produces unreliable output for high-stakes decisions
- The proposed **virtual credit committee**: specialized agents (Financial, Market, Team, Risk, Compliance) collaborate under a Manager agent to produce a consensus score, risk rating, confidence level, and full audit trail
- Enterprise-grade thinking spans six pillars: **security, data governance, network, operations, human factors, and compliance** — measured ROI showed 95% faster processing and 200–300% 3-year ROI

#### Friendly AI Assistant with Amazon Quick

- Business users face repetitive, time-consuming tasks that require pulling and analyzing information across multiple sources
- **Amazon Quick Suite** provides a unified, secure experience combining company data, world knowledge, 40+ data connectors, and agentic capabilities (automation flows, dashboards, chat, research) under one governed layer with guardrails and access controls
- Demoed use case: a PM assistant that automatically creates meeting minutes, emails stakeholders, and schedules follow-ups

#### From Edge to Origin: CloudFront as Your Foundation

- Usage-based CDN billing is hard to forecast — a bill can range from $0.03 to a $100K spike from viral traffic or attacks
- New **fixed-price CDN + security plans** (launching Nov 2025) bundle CloudFront, WAF, DDoS protection, Route 53, and CloudWatch logging into one predictable monthly price
- CloudFront materially improves **cost** (compression, free AWS-origin data transfer), **security** (TLS 1.3/mTLS, Origin Shield/OAC/VPC origins to cloak origins, signed URLs), **resiliency** (multi-layer caching, origin failover, graceful degradation), and **performance** (HTTP/3, persistent backbone connections, edge compute)

#### Context Is Everything

- Most disappointing AI answers come from **poor context, not bad models** — AI can't infer your goal or read your mind
- Common mistakes: dumping everything into a chat ("internet puller" problem), restating what the model already knows, and giving no goal/constraints/success criteria
- AI usage is evolving from single **prompts** → grounded **context** → persistent **memory** (store → retrieve → generate → learn), illustrated through a “Second AI Brain” case study
- A simple framework before asking AI anything: **Goal, relevant info, constraints, success criteria**

#### UTMorpho — Building a Product in 36 Hours (LotusHacks 2026)

- A team retrospective on going from “head empty” at sign-up to shipping UTMorpho within a 36-hour hackathon sprint
- Key challenges faced: AI overgeneration, token limits, and burnout close to pitch time — overcome through focused editing and better team sync
- Takeaway: **real frustration creates real ideas**, but more ideas are not automatically better ideas — endurance and team alignment matter as much as the tech

### Key Takeaways

#### AI Reliability Is a Design Problem, Not Just a Model Problem

- Determinism settings like `temp=0` reduce but don't eliminate randomness — build systems that tolerate variance
- Multi-agent architectures beat single agents for auditable, high-stakes, multi-domain decisions

#### Context Engineering Is Becoming a Core Skill

- Better context — not more context — drives better AI output
- The shift from prompting to context systems to long-term memory is the next skill gap to close

#### Infrastructure Foundations Still Matter

- CloudFront's edge capabilities (security, cost predictability, performance) are foundational even in an AI-heavy stack
- Enterprise-grade thinking (security, governance, compliance) must be designed in from day one, not bolted on later

### Applying to Work

- **Treat LLM output as probabilistic**: add majority-voting or structured-output constraints for any pipeline relying on `temp=0` for consistency
- **Prototype a multi-agent pattern** for any workflow currently forced onto a single, overloaded agent
- **Apply the four-part context framework** (goal, relevant info, constraints, success criteria) before writing prompts for real tasks
- **Evaluate CloudFront's fixed-price plans** for any project with unpredictable traffic to avoid bill-shock scenarios
- **Try Amazon Quick Suite** for repetitive business workflows (meeting notes, stakeholder updates, scheduling)

### Event Experience

Attending **“FCAJ Community Day”** was a great opportunity to see how different parts of the AWS community — from enterprise engineers to hackathon builders — are applying AI and cloud fundamentals in very different, very practical ways. Key experiences included:

#### Learning from community practitioners, not just official docs
- Speakers shared **first-hand findings**, like the LLM determinism research, rather than just marketing talking points.
- The startup credit scoring case study showed how **multi-agent design** solves real auditability problems in regulated industries like banking.

#### Connecting infrastructure and AI concerns
- The CloudFront session was a useful reminder that **edge and networking fundamentals** are still critical, even in an AI-centric roadmap.
- The context engineering talk reframed prompting as a **product experience problem**, not just a wording trick.

#### Seeing the builder side of the community
- The LotusHacks retrospective from Team VIB was a candid look at what a 36-hour build sprint actually feels like — including the failures, not just the demo.
- It reinforced that **team sync and endurance** are as important as raw technical skill under time pressure.

#### Lessons learned
- Reliability in AI systems has to be **engineered**, not assumed from a temperature setting.
- Good context design and good infrastructure design follow the same principle: **give the system exactly what it needs, no more, no less**.
- Community events like this surface practical lessons that are hard to find in official documentation alone.

#### Some event photos

![FCAJ Community Day - Event 2 photo 1](/images/4-Event/4.2-Event2/image2.png)

> Overall, the event connected AI reliability, agentic system design, context engineering, and cloud infrastructure fundamentals into one coherent picture — and reinforced that solid engineering practices matter just as much in the AI era as they always have.
