---
title: "Proposal: Estimated System Operating Costs on AWS"
date: 2026-06-21
weight: 2
chapter: false
pre: ""
---

# Estimated System Operating Costs on AWS

### Executive Summary

This document estimates AWS costs for the system of detecting and processing damaged goods in warehousing, based on serverless architecture using Amplify, Cognito, API Gateway, S3, SQS, Lambda, Rekognition, Textract, DynamoDB, SNS, CloudWatch, and IAM.

The estimate is built for a testing/actual operation scenario over 1 week, with a volume of approximately 245 images/week and ~30 active users. Within this assumption scope, the actual total cost of a new AWS account remains $0.00 because all usage falls within the corresponding Free Tier. If calculated at standard rates without applying Free Tier, the total cost for 1 week is approximately $1.57 USD.

---

### 1. System Architecture Overview

The serverless system on AWS is used to detect and process damaged goods in warehousing. Users access a web interface hosted on AWS Amplify, log in via Amazon Cognito to receive JWT tokens, then call APIs through Amazon API Gateway to upload goods images to Amazon S3.

When images are uploaded, S3 triggers events pushed to Amazon SQS to prevent overload when multiple images are sent simultaneously. SQS triggers a chain of AWS Lambda functions including image processing, calling Amazon Rekognition to detect damage, calling Amazon Textract to read tracking numbers or addresses on goods labels, then writing results to Amazon DynamoDB and sending alerts via Amazon SNS when AI confidence is below 80%.

The entire system is monitored by Amazon CloudWatch and applies the least-privilege principle through AWS IAM for each Lambda function. This report estimates AWS costs for 12 services appearing in the diagram, for one week of usage.

---

### 2. Usage Assumptions for Cost Estimation

The following assumptions are used as the basis for calculation:

- Image processing volume: approximately 35 images/day x 7 days, equivalent to 245 images/week.
- Active users: approximately 30 employees/customers logging in and using the web app during the week.
- AWS account: new account, still within 12 months of AWS Free Tier.
- Reference pricing region: US East (N. Virginia).

---

### 3. Cost Estimation Table by AWS Service (1 week)

| AWS Service | Estimated Usage Volume (1 week) | Reference Unit Price (US East, N. Virginia) | Cost at Standard Rates (without Free Tier) | AWS Free Tier Limits Applied | Actual Estimated Cost (new account, with Free Tier applied) |
| --- | --- | --- | --- | --- | --- |
| AWS Amplify (Web interface hosting) | ~5 builds, ~0.5 GB storage on CDN, ~0.5 GB data transfer for ~30 users | $0.01/build minute, $0.023/GB-month, $0.15/GB data transfer | ≈ $0.23 | 1,000 build minutes + 5 GB storage + 15 GB data transfer/month (first 12 months) | $0.00 |
| Amazon Cognito (Login authentication) | ~30 active users (MAU) | $0.015/MAU | ≈ $0.45 | 10,000 MAU/month | $0.00 |
| Amazon API Gateway (REST API) | ~1,800 API calls | $3.50/1 million calls | ≈ $0.006 | 1,000,000 calls/month (first 12 months) | $0.00 |
| Amazon S3 (Raw Image Bucket) | 245 PUT + 245 GET, ~0.5 GB storage | $0.005/1,000 PUT, $0.0004/1,000 GET, $0.023/GB-month | ≈ $0.004 | 2,000 PUT + 20,000 GET + 5 GB storage/month | $0.00 |
| Amazon SQS (Processing queue) | ~735 requests | $0.40/1 million requests | ≈ $0.0003 | 1,000,000 requests/month | $0.00 |
| AWS Lambda (3 functions) | ~800 invocations, ~800 GB-seconds | $0.20/1 million invocations + $0.0000166667/GB-second | ≈ $0.013 | 1,000,000 invocations + 400,000 GB-seconds/month | $0.00 |
| Amazon Rekognition (Damage detection) | 245 images processed | $0.001/image | ≈ $0.245 | 5,000 images/month (first 12 months) | $0.00 |
| Amazon Textract (Read shipping labels) | 245 pages | $0.0015/page | ≈ $0.368 | 1,000 pages/month (first 3 months) | $0.00 |
| Amazon DynamoDB (Log & history storage) | 245 writes + 300 reads | $0.625/1 million WRU, $0.125/1 million RRU | ≈ $0.0002 | 25 WCU/RCU + 25 GB storage/month | $0.00 |
| Amazon SNS (Send Email/SMS alerts) | ~25 alert emails | $2.00/100,000 emails sent | ≈ $0.0005 | 1,000 emails/month (first 12 months) | $0.00 |
| Amazon CloudWatch (Log, Metric, Alarm) | ~30 MB logs, 3-5 metrics, 3-5 alarms | $0.50/GB log, $0.30/metric-month, $0.10/alarm-month | ≈ $0.10 – $0.40 | 5 GB logs + 10 metrics + 10 alarms/month | $0.00 |
| AWS IAM (Least-privilege access control) | No usage-based fees | Free | $0.00 | Always free | $0.00 |

---

### 4. Cost Summary

**Total at standard rates (without Free Tier):** approximately $1.57 USD

Total actual estimated cost (new account, with Free Tier applied): **$0.00 USD**

The two lines above reflect two perspectives:

- Cost at standard rates if Free Tier were not available.
- Actual cost that will appear on the AWS bill during the testing week, equal to $0.00 because all usage falls within Free Tier limits.

---

### 5. Forecast for Scaling or Free Tier Expiration

If the system operates continuously for a full month, most services will still remain within monthly Free Tier limits. The most important point to note is Amazon Textract because the free limit only lasts for the first 3 months. However, at the current scale, the total monthly AWS cost is expected to remain very low, even without Free Tier.

---

### 6. Estimation Limitations and Recommendations

- This is an estimate based on traffic assumptions, not actual billing data.
- The most accurate figures are direct monitoring in AWS Cost Explorer after the system runs in production.
- Reference prices according to US East (N. Virginia) region; prices in other regions may vary.
- Does not include costs outside the diagram scope such as Support Plan, domain, Route 53, WAF, or operating personnel costs.

---

### 7. References

- AWS Lambda Pricing: https://aws.amazon.com/lambda/pricing/
- Amazon API Gateway Pricing: https://aws.amazon.com/api-gateway/pricing/
- Amazon S3 Pricing: https://aws.amazon.com/s3/pricing/
- Amazon SQS Pricing: https://aws.amazon.com/sqs/pricing/
- Amazon Rekognition Pricing: https://aws.amazon.com/rekognition/pricing/
- Amazon Textract Pricing: https://aws.amazon.com/textract/pricing/
- Amazon DynamoDB Pricing: https://aws.amazon.com/dynamodb/pricing/on-demand
- Amazon SNS Pricing: https://aws.amazon.com/sns/pricing/
- Amazon Cognito Pricing: https://aws.amazon.com/cognito/pricing/
- Amazon CloudWatch Pricing: https://aws.amazon.com/cloudwatch/pricing/
- AWS Amplify Pricing: https://aws.amazon.com/amplify/pricing/
- AWS Free Tier: https://aws.amazon.com/free/

