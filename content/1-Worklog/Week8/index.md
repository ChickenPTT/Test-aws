---
title: "Worklog Week 8"
date: 2026-06-22
weight: 1
chapter: false
pre: ""
---

### Week 8 Goals:

- Draw the structure/architecture of the project within 2 days.
- Finalize the architecture diagram for the proposal and workshop.
- Practice the main content in the workshop.
- Start editing workshop content into a clear report file.

### Tasks to complete this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | **Draw project structure - Day 1** <br>&emsp; + Identify architecture layers: Frontend/Auth, Storage, Backend/AI-ML, Monitoring/Security <br>&emsp; + Sketch the processing flow from image upload to result storage <br>&emsp; + Select appropriate AWS services for each layer | 06/22/2026 | 06/22/2026 | [Proposal](/Content/2.%20Proposal/_proposal.md) |
| 3 | **Draw project structure - Day 2** <br>&emsp; + Finalize architecture diagram <br>&emsp; + Review the S3 -> SQS -> Lambda -> Rekognition/Textract -> DynamoDB flow <br>&emsp; + Add CloudWatch and IAM to the diagram | 06/23/2026 | 06/23/2026 | [DiagramStructure](/Content/2.%20Proposal/image/DiagramStructure.png) |
| 4 | **Practice workshop content** <br>&emsp; + Prepare IAM Role for Lambda <br>&emsp; + Create SQS queue to receive image processing events <br>&emsp; + Configure S3 bucket and event notification | 06/24/2026 | 06/24/2026 | [Workshop](/Content/5.%20Workshop/1.WorkShop-overview/OverView.md) |
| 5 | **Edit workshop report** <br>&emsp; + Review overview, IAM, SQS, S3 sections <br>&emsp; + Standardize descriptions for each practice step <br>&emsp; + Add illustrative images and verification results | 06/25/2026 | 06/25/2026 | [Workshop](/Content/5.%20Workshop/1.WorkShop-overview/OverView.md) |

### Week 8 Results Achieved

**Architecture Design:**

- Completed overall project structure:
  <br> + Frontend/Auth using Amplify, Cognito, API Gateway
  <br> + Storage using Amazon S3
  <br> + Backend processing using SQS and Lambda
  <br> + AI/ML using Rekognition and Textract
  <br> + Data layer using DynamoDB
  <br> + Monitoring/Security using CloudWatch and IAM

**Workshop Practice:**

- Practiced foundational steps of the workshop:
  <br> + Create IAM Role
  <br> + Create SQS queue
  <br> + Configure S3
  <br> + Prepare Lambda function

- Started converting workshop practice content into a clearly structured workshop report.