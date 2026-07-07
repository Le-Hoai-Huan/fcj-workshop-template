---
title: "Event 4"
date: 2026-06-06
weight: 4
chapter: false
pre: " <b> 4.4. </b> "
---


# Summary Report: “FCAJ Community Day”

**Date & Time:** 09:00, 06 June, 2026

### Event Objectives

- Showcase real member-built projects spanning security, game networking, and generative AI on AWS
- Share practical career journeys — from helpdesk to senior sysadmin, and from student to cloud/security engineer
- Introduce foundational technology (Docker) and applied AI architecture (GraphRAG) through hands-on sessions
- Reinforce the teamwork practices that make technical projects and hackathons actually ship

### Speakers

- **Le Hoang Gia Dai** – Team AWS G3 - *AWS WAF + Machine Learning NIDS for Cyber Attack Detection*
- **Bao Huynh** – Junior Cloud Native Developer, Endava Vietnam / Founder, ITea Lab - *Docker – A Containerization Technology*
- **Tran Trung Vinh** – System Administrator, Central Retail Group - *From IT Helpdesk to Senior Sysadmin*
- **Nguyen Quoc Bao** – *Multiplayer in the Cloud: Connecting Godot Clients with AWS WebSockets*
- **Truong Huy Phuoc** – *The Art of Effective Teamwork*
- **Viet Phat** – AI major, Swinburne University of Technology - *GraphRAG: Building GraphRAG Applications with Amazon Bedrock and Amazon Neptune*

### Key Highlights

#### AWS WAF + Machine Learning NIDS for Cyber Attack Detection

- **AWS WAF** protects CloudFront, ALB, API Gateway, and Cognito against common exploits (SQLi, XSS, bot traffic, brute force) using rule-based detection — effective against known patterns, but weak against zero-day and novel/hybrid attacks.
- To go beyond static rules, the project built a **Machine Learning-based NIDS** trained on the CSE-CIC-IDS2018 dataset (University of New Brunswick): merging raw CSVs, cleaning invalid/NaN/infinite values, removing unneeded columns, and rebalancing attack classes before training a **LightGBM** model.
- Full architecture on AWS: VPC, EC2, ALB, WAF, S3, Kinesis Data Firehose, Lambda, Security Hub, GuardDuty, Inspector, SNS, IAM, Config, CloudWatch — correlating ML NIDS predictions with WAF events in a real-time dashboard for stronger detection than either signal alone.
- Lessons learned: data quality and class balance drive ML performance; signature-based protection alone is insufficient; ML-based NIDS meaningfully complements AWS WAF rather than replacing it.

#### Docker – A Containerization Technology

- Virtual machines each carry their own OS, consuming more CPU/memory/storage and needing separate updates — too heavy for many small apps.
- **Containerization** packages an app with everything it needs into one unit that runs consistently anywhere, sharing the host OS kernel — making containers far more lightweight than VMs.
- **Docker**'s core idea: *build once, run anywhere*. Each Dockerfile instruction creates an image layer; Docker reuses unchanged cached layers and only rebuilds a layer (and everything after it) when something changes.
- Common use cases: CI/CD pipelines, microservices architectures, dev/test environments, cloud-native applications, and legacy application modernization.

#### From IT Helpdesk to Senior Sysadmin

- A career built without a top-university degree: starting in IT Helpdesk, the core transferable skills were troubleshooting under pressure, end-user communication, and a problem-solving mindset — the turning point came from self-teaching Linux, networking, and building hands-on lab environments.
- Life as a sysadmin goes beyond servers: provisioning, network management, patching, and capacity planning. Key lessons — automate repetitive tasks, document configs and runbooks, monitor *before* incidents happen, and **never test in production**.
- The move from Sysadmin to Cloud/DevOps was a mindset shift, not just a tool change: on-premise manual scaling → AWS elastic, pay-as-you-go infrastructure → Infrastructure as Code with Terraform → a DevOps culture of CI/CD, Docker, and closer collaboration with developers.
- Interview and career advice: real projects and practical experience outweigh certifications alone; common mistakes are learning too many things at once, not practicing enough, and being afraid to fail — go deep on 1-2 core skills first, and remember that **where you start doesn't matter, only that you keep going**.

#### Multiplayer in the Cloud: Godot + AWS WebSockets

- Choosing the right networking model matters: **UDP/ENet** for low-latency FPS/racing games, **WebSocket** for turn-based/lobby/chat needs full-duplex reliable delivery, and **HTTP polling** for simple, stateless needs like login or leaderboards.
- Architecture built for a turn-based matchmaking demo: Godot client → **API Gateway WebSocket** (`$connect`/`$disconnect`/`$default` routes) → **Lambda** (Node.js) → **DynamoDB** (`connectionId` as partition key, tracking status/opponent/choice) → CloudWatch for logs.
- On the client side, Godot's `WebSocketPeer` handles the connection; polling every frame drives the game loop, sending/receiving JSON messages to progress through matchmaking, choice submission, and result resolution.
- Real challenges surfaced in production: **stale connections** (`GoneException`) when a disconnected player is still in DynamoDB, **DynamoDB Scan cost** growing with player count, and Lambda's **statelessness** forcing a DynamoDB round-trip on every request.
- Looking ahead: today's WebSocket + Lambda approach fits turn-based games well, while **AWS GameLift** is the better fit for continuous, high-frequency real-time games needing persistent in-memory state and dedicated servers.

#### The Art of Effective Teamwork

- Four golden rules for effective teams: **clear & shared goals**, **right person in the right place**, **open communication & active listening**, and **personal accountability**.
- Practical digital tools to support teamwork: Trello and ClickUp for task tracking, Google Workspace and Slack for collaboration and communication, and Discord for real-time team coordination.

#### GraphRAG: Building GraphRAG Applications with Amazon Bedrock and Amazon Neptune

- **RAG** augments an LLM at runtime by retrieving relevant passages from a knowledge base and injecting them into the prompt — but standard RAG struggles with **multi-hop questions** (e.g., "where is the company headquartered that was acquired by the company founded by Jeff Bezos?") because it can't reason across chained relationships.
- **GraphRAG** solves this by storing relationships explicitly as graph edges and using graph traversal for **multi-hop reasoning** across multiple entities and documents.
- Two implementation paths were compared: the **fully managed route** using Amazon Bedrock Knowledge Bases (chunking, entity extraction, embeddings) plus Amazon Neptune Analytics (graph storage, relationship discovery); and the **custom route** using a LlamaIndex processing pipeline plus Amazon Neptune with direct Cypher queries for multi-hop traversal.

### Key Takeaways

#### Layered Defense Beats Any Single Security Control

- Rule-based tools like AWS WAF and learned/behavioral tools like ML-based NIDS catch different classes of attacks — combining their signals outperforms relying on either alone

#### Right Tool for the Right Constraint

- Containerization vs. virtualization, WebSocket vs. UDP vs. HTTP polling, fully managed vs. custom GraphRAG — the recurring lesson is choosing an approach based on the actual constraint (resource weight, latency, control) rather than defaulting to what's familiar

#### Career Growth Rewards Depth and Real Practice Over Credentials

- Both the sysadmin and security-engineer journeys shared a common thread: hands-on labs, real projects, and going deep on a few fundamentals mattered more than formal pedigree or certification alone

#### Distributed Systems Fail at the Edges (Stale State, Cost at Scale)

- The multiplayer NIDS/WebSocket architectures both surfaced the same class of problem — state that outlives a connection or scan costs that grow with data — a reminder to design for cleanup and scale from day one

#### Technical Delivery Still Depends on Team Fundamentals

- None of the above matters without clear goals, the right people in the right roles, and honest communication — the "soft" teamwork rules underpin whether any of the technical work ships

### Applying to Work

- **Layer detection controls**: pair rule-based tools (WAF) with anomaly/ML-based detection where the threat model includes novel attack patterns
- **Default to containers** for new services unless there's a specific reason to need full VM isolation
- **Match the networking model to the use case** — don't reach for WebSockets or raw UDP by default; check latency and reliability needs first
- **Invest in 1-2 deep skills** and a real portfolio project before spreading effort across many certifications
- **Plan for connection/state cleanup explicitly** in any serverless + WebSocket or pub/sub architecture, rather than discovering it in production
- **Evaluate GraphRAG** (managed or custom) for any RAG use case that requires reasoning across relationships, not just single-document retrieval
- **Revisit the 4 teamwork rules** (shared goals, right person/role, open communication, accountability) at the start of any new project or hackathon team

### Event Experience

Attending this session of **“FCAJ Community Day”** was a great showcase of how varied "building on AWS" can look — from cybersecurity and game networking to generative AI and plain old sysadmin fundamentals. Key experiences included:

#### Seeing security as a layered, evolving problem
- Le Hoang Gia Dai's WAF + ML NIDS project was a concrete example of combining rule-based and learned defenses, and a reminder that **no single control is enough** against evolving attacks.

#### Getting a clear, practical grounding in containers
- Bao Huynh's Docker session made the VM-vs-container tradeoff tangible, reinforcing why containers have become the default building block for modern deployments.

#### Hearing a career story that didn't start with a "perfect" resume
- Tran Trung Vinh's journey from IT Helpdesk to Senior Sysadmin (and into Cloud/DevOps) was a grounded reminder that consistent hands-on practice can matter more than where you start.

#### Watching real-time multiplayer infrastructure built and explained end-to-end
- Nguyen Quoc Bao's Godot + AWS WebSocket demo connected client-side game code to serverless backend design in a way that made the tradeoffs (and the failure modes) very concrete.

#### Being reminded that shipped projects are still a team sport
- Truong Huy Phuoc's teamwork talk was a good gut-check: none of the technical sessions above would have shipped without clear goals, the right roles, and honest communication inside the team.

#### Getting a hands-on look at where RAG breaks down — and how GraphRAG fixes it
- Viet Phat's GraphRAG session made a fuzzy "RAG isn't enough for complex questions" complaint concrete by showing exactly which multi-hop questions plain RAG fails on, and how Bedrock + Neptune (managed or custom) can close that gap.

#### Lessons learned
- Combining complementary techniques (rules + ML, containers + orchestration, RAG + graphs) consistently beats relying on one approach alone.
- Real-world distributed systems (WebSocket backends, ML pipelines) fail at the edges — stale state and scaling cost — so design for cleanup early.
- Career and project outcomes both depend as much on fundamentals and teamwork as on the specific technology chosen.

#### Some event photos

![FCAJ Community Day - Event 4 photo 1](/images/4-Event/4.4-Event4/image5.png)
![FCAJ Community Day - Event 4 photo 2](/images/4-Event/4.4-Event4/image6.png)


> Overall, this session of FCAJ Community Day connected cybersecurity, containerization, career growth, real-time game networking, teamwork, and applied generative AI into one picture: strong technical building blocks only turn into shipped, resilient projects when paired with fundamentals and the right team practices.
