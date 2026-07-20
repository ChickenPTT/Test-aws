---
title: "Project Proposal"
date: 2026-06-21
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Automated Goods Quality Monitoring Solution Based on Serverless and AI/ML

### Executive Summary

In the Logistics field, businesses are under significant pressure regarding processing time, data accuracy, and the ability to control goods loss. Current goods quality monitoring in warehouses largely depends on human labor, leading to slow incident handling, scattered data, and difficulty in real-time updates.

The team proposes building a system **"Automated Goods Quality Monitoring Solution Based on Serverless Architecture and Artificial Intelligence (AI/ML)"**. This is a software system applying Amazon Web Services (AWS) services, allowing delivery staff or customers to take photos of goods with incidents such as tears, breaks, dents, or damage, then directly upload images to the system for automatic analysis.

The system uses AI/ML to identify the degree of goods damage, extract shipping information, store evidence, and send alerts to relevant departments. As a result, the incident handling process can be shortened from several hours or days to just a few seconds, while helping businesses reduce operating costs, limit manual errors, and improve service quality.

---

### Problem Statement

#### Current Issues

According to practical surveys, the recording and handling of damaged goods currently encounters many operational issues:

- **Manual, time-consuming, and error-prone process:** When discovering damaged goods, employees often have to take photos with personal phones, send them via chat groups, or create paper reports. The appraisal department then has to compile this scattered information to re-enter into the ERP system and process compensation procedures for customers. This process takes time and easily causes data confusion.

- **Lack of automation and real-time alerts:** Since there is no software to automatically analyze images and read order information, warehouse managers often do not immediately know the extent of goods damage to make timely handling decisions. Slow feedback affects customer experience and service reputation.

- **Lack of system scalability:** During peak seasons, the volume of goods arriving at warehouses increases significantly. Manual inspection processes cannot handle multiple orders simultaneously, leading to overload, missed damaged goods, or allowing defective products to continue reaching consumers.

- **Fragmented data storage, difficult to retrieve:** Current incident records may be scattered in notebooks, Excel files, or chat groups. When needing to统计 loss rates by month/quarter to report to the board of directors, employees have to manually review, which is time-consuming and prone to errors.

- **High operating costs:** Businesses must maintain dedicated personnel at each warehouse point to inspect, enter data, and handle incidents. Besides labor costs, information errors and prolonged compensation disputes also reduce the profits and reputation of Logistics businesses.

---

### Proposed Solution

The team proposes building a system to automate the goods quality monitoring process based on Serverless and AI/ML architecture. The system focuses on the following core capabilities:

- **Smart AI automation:** The system uses Amazon Rekognition to analyze goods images and identify signs of damage. Analysis results can include status labels, damage levels, and confidence scores. Amazon Textract is used to extract tracking numbers, addresses, or related text information from images without manual entry.

- **Real-time asynchronous processing:** After images are uploaded to Amazon S3, an automatic processing flow is triggered. Image data, tracking numbers, and analysis results are synchronized to Amazon DynamoDB for lookup, statistics, and report generation. This processing method helps shorten recording and response time from several days to just a few seconds.

- **Auto-scaling Serverless infrastructure:** The system runs on AWS Serverless services, which can automatically scale when the number of images increases suddenly during peak seasons. Businesses do not need to manually manage servers but still ensure the ability to handle multiple requests simultaneously.

- **Centralized and transparent data management:** All scan history, evidence images, tracking numbers, and processing status are stored centrally. Managers can look up history at any time, check evidence, and export statistical reports on damaged goods situations.

- **Operating cost optimization:** Bringing AI into the process helps reduce errors compared to manual entry, reduces the need for dedicated personnel at each warehouse, shortens dispute resolution time, and increases reliability in compensation processing.

---

### Solution Architecture

#### Overall Architecture
<div style="display: flex; gap: 10px; justify-content: center; flex-wrap: wrap;">
      <img src="/images/2-Proposal/DiagramStructure.png" alt="" width="1939" />

</div>

The system is designed according to event-driven architecture, using AWS services to automatically scale according to actual traffic. The entire lifecycle of a goods quality monitoring request is divided into 4 main technology layers:

| Architecture Layer | Role | Proposed AWS Services |
| --- | --- | --- |
| Frontend & Auth | Provides web interface, manages login/registration, issues JWT Token and controls API access | AWS Amplify, Amazon Cognito, Amazon API Gateway |
| Storage | Receives and stores damaged goods images uploaded by users | Amazon S3 |
| Backend & AI/ML | Processes image upload events, analyzes images, extracts shipping information, evaluates damage levels, and updates data | Amazon SQS, AWS Lambda, Amazon Rekognition, Amazon Textract, Amazon DynamoDB |
| Monitoring & Security | Monitors system activity, manages logs, controls access according to least privilege principle | Amazon CloudWatch, AWS IAM |

#### Main Processing Flow

| Step | Description |
| --- | --- |
| 1 | Users log into the system through the web interface deployed by AWS Amplify and authenticated by Amazon Cognito. |
| 2 | Users upload images of damaged goods to the system. Images are stored in Amazon S3 Raw Image Bucket. |
| 3 | S3 Event Notification generates an event after the image is successfully uploaded and puts processing information into Amazon SQS. |
| 4 | Lambda orchestrator-function reads events from SQS, then calls Amazon Rekognition to detect damage and Amazon Textract to read tracking numbers/text information. |
| 5 | Lambda evaluator-function evaluates the damage level based on AI/ML results and determines processing status. |
| 6 | Lambda processor-function saves results to Amazon DynamoDB, updates record status, and triggers alerts if needed. |
| 7 | Amazon SNS sends Email/SMS notifications to warehouse managers or processing departments when serious incidents are detected. |
| 8 | Amazon CloudWatch records logs, metrics, and supports error tracking throughout the operation process. |

---

### AWS Services Used

#### Frontend & Auth

- **AWS Amplify:** Hosts and distributes the web interface for users.
- **Amazon Cognito:** Manages login, registration, and issues JWT Token.
- **Amazon API Gateway:** Receives API requests, validates tokens, and forwards requests to the backend.

#### Storage

- **Amazon S3:** Stores original images of goods, serving as the data entry point for the entire system. Images are organized into separate buckets for raw images and processed results.

#### Backend & AI/ML

- **Amazon SQS:** Queue service for asynchronous processing, helps prevent system overload when multiple images are uploaded simultaneously.
- **AWS Lambda:** Serverless compute service that processes images, calls AI/ML services, and updates data without managing servers.
- **Amazon Rekognition:** AI service for image analysis, detects signs of damage on goods.
- **Amazon Textract:** AI service for extracting text and tracking numbers from images automatically.
- **Amazon DynamoDB:** NoSQL database for storing scan history, processing results, and tracking information.

#### Monitoring & Security

- **Amazon CloudWatch:** Monitoring service that tracks system activity, collects logs, and sets up alerts for unusual activities.
- **AWS IAM:** Identity and access management service, applies least privilege principle for each Lambda function.

---

### Benefits

- **Reduces incident handling time:** From several hours/days to just a few seconds.
- **Improves data accuracy:** Automated analysis reduces human errors in data entry.
- **Cost optimization:** Serverless architecture only pays for actual usage, no need to maintain servers.
- **Enhances customer experience:** Fast and transparent incident handling process.
- **Scalability:** System automatically scales during peak seasons without manual intervention.
- **Data transparency:** Centralized storage makes tracking and reporting easier.

---

### Conclusion

The proposed solution leverages AWS Serverless and AI/ML services to automate the goods quality monitoring process, addressing current operational challenges in Logistics. The system not only improves efficiency and accuracy but also optimizes costs and enhances service quality for businesses.
