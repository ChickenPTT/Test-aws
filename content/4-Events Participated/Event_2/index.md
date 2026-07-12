---
title: "AWS AI & Cloud Operations Workshop"
date: 2026-06-12
weight: 4
chapter: false
pre: " <b> 4.3. </b> "
---

# "AWS AI & Cloud Operations Workshop" Learning Summary

### Purpose of the Event

- Get up to date on trends in applying AI Agents to cloud infrastructure operations, DevOps, and incident handling.
- Explore real-world problems in AI Voice, Vietnamese language processing, response latency, and natural conversational experience.
- Discover how AI supports businesses in recruitment, onboarding, candidate evaluation, and HR process optimization.
- Connect the event's knowledge to an AWS cost-estimation proposal for a serverless system that handles damaged goods.

### List of Speakers

- **Truong Tran** – AI Solution Sales, Noventiq
- **Steve Tran** – CTO/Founder, CloudThinker
- **Trung Vu** – CEO, Revve AI
- **Anh Dang** – Solution Sales, Noventiq
- **Nghi Danh** – AI Engineer, Renova Cloud
- **Kiet Tran** – AI Engineer, AWS Student Builder Group
- **Bao Phan** – Cloud Engineer, Cloud Kinetics
- **Nguyen Nguyen** – Cloud Engineer, Cloud Kinetics
- **Toan Nguyen** – AWS Security Builder

---

### Highlights

#### AgenticOps for Your Cloud

Speaker **Steve Tran** shared insights on the current state of cloud operations in complex microservices systems. When logs, tracing, metrics, and alerts are scattered across many locations, operations engineers often spend a great deal of time investigating the root cause of an incident.

- **The current state of cloud operations**: Modern systems consist of many independent components, which makes monitoring, error tracing, and incident response more difficult.
- **The AgenticOps solution**: AI Agents are used to automate investigation steps, aggregate data, and suggest remediation directions, helping reduce analysis time from hours down to just minutes.
- **Operating process**:
    - **Classification**: Categorizing incidents from alerts or direct requests.
    - **Investigation**: Analyzing logs, metrics, topology, and hypothesizing causes.
    - **Mitigation**: Suggesting safe remediation options for the engineer to decide on.
    - **Optimization**: Proposing long-term improvements to prevent recurrence.

#### The Voice of AI (AI Voice)

The session by **Trung Vu**, **Nghi Danh**, and **Kiet Tran** focused on how to build a low-latency conversational voice experience suited to Vietnamese users.

- **Latency requirements**: For natural conversation, the system needs to process via a streaming mechanism from Speech-to-Text through the LLM to Text-to-Speech, rather than waiting for the user to finish speaking an entire command.
- **Challenges specific to Vietnamese**: AI needs to understand forms of address, gender, communication context, and linguistic nuance to avoid responses that feel unnatural or disrespectful.
- **Handling regional accents**: Training data needs an appropriate proportion of regional accents to improve recognition, while still being controlled so the AI doesn't unprofessionally mimic a local accent automatically.

#### Technical Aspects and Real-World Applications of DevOps Agents

The speakers illustrated a scenario where a website becomes slow or fails due to a sudden spike in request traffic. In traditional systems, engineers have to manually access multiple dashboards to gather logs, tracing, and metrics. With an AI Agent, this process can be automated in a controlled manner.

- **Incident Investigation**: The AI Agent aggregates observed data, builds a system topology, and generates hypotheses about the cause of the failure.
- **Extensibility**: The Agent can integrate with MCP (Model Context Protocol), Slack, ServiceNow, or other operational tools.
- **Security note**: The Agent should only access data it has been explicitly granted permission to. If logs haven't been exported to CloudWatch or a centralized observability system, the Agent should not attempt to SSH into servers to retrieve data on its own.
- **Live demo**: A simulated DDoS scenario with 1,000 requests/second hitting an ALB — the AI Agent detected 10 ECS Tasks being spammed and suggested commands to stop the affected tasks.

#### Real-World Case Studies

- **An online university**: Reduced MTTR from 2 hours to just 28 minutes, roughly a 77% improvement.
- **Zenchef, a restaurant tech platform**: Detected a configuration error within about 20 minutes.

#### AI and Human Resources in Business

The presentation by **Truong Tran** and **Anh Dang** covered how AI supports HR departments in recruitment and personnel management.

- **Retaining talent**: Businesses need to reduce the risk of losing staff after the training and onboarding process.
- **Candidate evaluation**: AI helps match CVs against job descriptions, checking skills, experience, and overall fit.
- **Automating onboarding**: Shortening the time it takes for new hires to get up to speed with processes, documentation, and internal systems.
- **No-code/low-code with Amazon Q**: HR staff can build recruitment management apps or resume-analysis tools without complex programming.
- **Live demo**: Amazon Q was used to draft a job description for a Junior Cloud Engineer role and compare candidates based on technical skills, problem-solving ability, communication, and appropriate salary benchmarks.

---

### Key Takeaways

#### A Mindset for Cloud Operations with AI Agents

- Understood clearly that an AI Agent doesn't fully replace operations engineers, but instead acts as an assistant that analyzes data, gathers context, and suggests remediation options.
- Recognized the importance of observability in the cloud: logs, metrics, tracing, and alerts must be well designed for the Agent to have reliable data to analyze.
- Grasped the incident-handling process through the steps of classification, investigation, impact mitigation, and long-term optimization.

#### Techniques for Building AI Voice Applications

- Learned that the AI Voice experience depends heavily on latency and the ability to stream continuously between components.
- Gained a clearer understanding of the unique challenges of Vietnamese, such as forms of address, regional accents, and communication context.
- Understood that training data must be carefully curated to balance accuracy, naturalness, and professionalism.

#### Applying AI in Business

- AI can help automate repetitive tasks in recruitment, CV analysis, interview scheduling, and onboarding support.
- Tools like Amazon Q help business users build internal applications faster, especially in processes involving a lot of data and evaluation criteria.
- When applying AI in a business context, attention must be paid to data access permissions, transparency, and ensuring humans retain control over final decisions.

---

### Applications to AWS Proposals and Projects

- **Designing operations for a serverless system**: AgenticOps knowledge can be applied to a system for detecting and handling damaged goods on AWS by standardizing logs from Lambda, API Gateway, SQS, S3, Rekognition, Textract, and DynamoDB into CloudWatch.
- **Cost optimization through observability**: The AWS cost proposal shows the test system still fits within the Free Tier. However, as it scales, usage metrics for each service need to be monitored to control costs and detect anomalies early.
- **Increasing reliability of the image-processing workflow**: An AI Agent can help catch errors in the S3 → SQS → Lambda → Rekognition/Textract → DynamoDB pipeline, especially when image processing fails or AI confidence is low.
- **Improving user experience**: AI Voice knowledge could be extended in the future to a voice-based data-entry feature, helping warehouse staff report goods status more quickly.

---

### Experience at the Event

The event offered a practical perspective on how AI is being incorporated into cloud operations, DevOps, and business processes. Notably, the presentations didn't just discuss general AI concepts — they went deep into immediately applicable scenarios such as incident investigation, log analysis, MTTR reduction, Vietnamese voice processing, and recruitment automation.

- **A hands-on learning environment**: Attendees heard concrete case studies from cloud operations, AI Voice, and HR automation.
- **Clear technical perspective**: The speakers explained how AI Agents work together with telemetry, MCP, CloudWatch, and other operational tools to support engineers.
- **Strong relevance to personal projects**: The event's content reinforced the idea that designing an AWS system isn't just about making it work — it also needs to be observable, cost-controllable, and easy to troubleshoot.

#### Some photos from the event

<div style="display: flex; gap: 10px; justify-content: center; flex-wrap: wrap;">
  <img src="/images/4-Events-Participated/Image_event/event2-1.png" alt="AWS AI and Cloud Operations Workshop 1" width="45%" />
  <img src="/images/4-Events-Participated/Image_event/event2-2.png" alt="AWS AI and Cloud Operations Workshop 2" width="45%" />
</div>