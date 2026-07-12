---
title: "Worklog Week 2"
date: 2026-05-04
weight: 1
chapter: false
pre: ""
---

### Week 2 Objectives:

- Build a solid foundation in Amazon EC2 and its core features such as Instance types, AMI, Snapshots
- Practice deploying a Node.js application on EC2 instances running Amazon Linux and Windows
- Understand how to manage access permissions and limit resource usage using AWS IAM
- Get familiar with the AWS Cloud9 IDE for developing applications directly on the cloud
- Master hosting a static website on Amazon S3 with advanced features
- Optimize website performance using CloudFront CDN
- Manage object versioning and perform data replication between regions on S3

### Tasks to complete this week:

| Day | Task                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Start Date | Completion Date | Reference Materials                                                                                              |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | ---------------- | ------------------------------------------------------------------------------------------------------------------ |
| 2   | **Hands-on lab: Getting started and deploying an application on Amazon Compute Cloud (Amazon EC2)** <br>&emsp; + Introduction to AWS (Amazon Elastic Compute Cloud) - EC2 <br>&emsp;&emsp; • Instance type <br>&emsp;&emsp; • AMI/Backup/Keypair <br>&emsp; + Preparation steps: <br>&emsp;&emsp; • Create VPC for Linux/Windows <br>&emsp;&emsp; • Security group for Linux/Windows <br>&emsp; + Launch a Windows/Linux instance <br>&emsp; + EC2 basics: <br>&emsp;&emsp; • Change EC2 configuration <br>&emsp;&emsp; • Create a snapshot <br>&emsp;&emsp; • Custom AMI <br>&emsp;&emsp; • Create an instance from a Custom AMI <br>&emsp;&emsp; • Access EC2 after losing the keypair (Linux and Windows) <br>&emsp;&emsp; • Configure a desktop GUI for EC2-ubuntu 22.04 <br>&emsp;&emsp; • Amazon EBS Snapshot archive                                                                                                                                                                                                                                                                                                                                                                             | 05/11/2026 | 05/12/2026        | <https://000004.awsstudygroup.com/vi/5-amazonec2basic/>                                                            |
| 3   | **Continue completing the EC2 hands-on lab** <br>&emsp; + Deploy a Node.js app on Amazon Linux: <br>&emsp;&emsp; • Download the LAMP web server <br>&emsp;&emsp; • Prepare LAMP <br>&emsp;&emsp; • Configure and install phpMyAdmin <br>&emsp;&emsp; • Install Node.js on Linux <br>&emsp;&emsp; • Deploy the app on the Linux instance <br>&emsp; + Deploy a Node.js app on Amazon Windows: <br>&emsp;&emsp; • Install XAMPP on the Windows instance <br>&emsp;&emsp; • Install Node.js on the Windows instance <br>&emsp;&emsp; • Deploy on the Windows instance <br>&emsp; + Limit resource usage using the IAM service <br>&emsp;&emsp; • Restrict usage to a specific Region <br>&emsp;&emsp; • Restrict EC2 by instance family <br>&emsp;&emsp; • Restrict EC2 by instance type <br>&emsp;&emsp; • Restrict EBS volume <br>&emsp;&emsp; • Restrict resource deletion permissions <br>&emsp;&emsp; • Restrict resource deletion by time window <br> **Hands-on lab: Granting application access to AWS services with IAM Role** <br>&emsp; + Create an EC2 instance <br>&emsp; + Create an S3 bucket <br>&emsp; + Use an access key: create an IAM user, access key, and use the access key <br>&emsp; + Create an IAM role <br>&emsp; + Use the IAM role | 05/12/2026 | 05/12/2026        | <https://000048.awsstudygroup.com/vi/3-iamroleec2/> <br> <https://000004.awsstudygroup.com/vi/5-amazonec2basic/> |
| 4   | **Hands-on lab: Using a browser-based Cloud IDE with AWS Cloud9** <br>&emsp; + Overview of AWS Cloud9 <br>&emsp; + Create a Cloud9 instance <br>&emsp; + Basic features: <br>&emsp;&emsp; • Using the command line <br>&emsp;&emsp; • Working with text files <br>&emsp;&emsp; • Dashboard interface <br>&emsp; + Using the AWS CLI <br> **Hands-on lab: Hosting a static website with Amazon S3** <br>&emsp; + General theoretical overview <br>&emsp; + Create an S3 bucket <br>&emsp; + Upload data <br>&emsp; + Enable static website hosting <br>&emsp; + Configure Block Public Access <br>&emsp; + Configure public object access <br>&emsp; + Test the website                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 05/13/2026 | 05/14/2026        | <https://000057.awsstudygroup.com/vi/1-introduce/> <br> <https://000049.awsstudygroup.com/vi/>                     |
| 5   | **Hands-on lab: Hosting a static website with Amazon S3 (continued)** <br>&emsp; + Speed up the static website with CloudFront <br>&emsp; + Block public access to S3 <br>&emsp; + Configure Amazon CloudFront <br>&emsp; + Verify Amazon CloudFront <br>&emsp; + Bucket versioning: <br>&emsp;&emsp; • Introduction <br>&emsp;&emsp; • How it works <br>&emsp;&emsp; • Step-by-step guide <br>&emsp; + Move an Object <br>&emsp; + Replicate an S3 Object to another region                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | 05/14/2026 | 05/14/2026        | <https://000057.awsstudygroup.com/vi/1-introduce/>                                                                 |

### Week 2 Results Achieved

**EC2 Core Knowledge:**

- Solid understanding of EC2 concepts:
  <br> + Instance types
  <br> + AMI, Backup, Keypair
  <br> + Security Groups and VPC configuration
  <br> + Snapshots and Custom AMI
  <br> + Handling lost keypairs for both Linux and Windows
  <br> + Desktop GUI setup for EC2-ubuntu 22.04
  <br> + Amazon EBS Snapshot archive

- Node.js application deployment:
  <br> + LAMP stack setup on Amazon Linux
  <br> + phpMyAdmin configuration
  <br> + Node.js installation on Linux instance
  <br> + Node.js app deployment on Linux
  <br> + XAMPP setup on Windows instance
  <br> + Node.js installation on Windows instance
  <br> + Node.js app deployment on Windows

**IAM Resource Control:**

- Restricting resource usage with IAM policies:
  <br> + Region-specific access control
  <br> + Instance family restrictions
  <br> + Instance type limitations
  <br> + EBS volume quotas
  <br> + Resource deletion permissions
  <br> + Time-based resource deletion policies

**IAM Role Practice:**

- Practicing permission granting with IAM Roles:
  <br> + EC2 instance creation and configuration
  <br> + S3 bucket setup
  <br> + IAM user and access key management
  <br> + IAM role creation and usage
  <br> + Application access to AWS services

**AWS Cloud9 IDE:**

- Solid understanding of AWS Cloud9 concepts:
  <br> + Cloud IDE overview
  <br> + Cloud9 instance creation
  <br> + Command line usage
  <br> + Text file editing
  <br> + Dashboard interface
  <br> + AWS CLI integration

**Amazon S3 Static Website Hosting:**

- Hosting a static website on S3:
  <br> + S3 bucket creation
  <br> + Data upload
  <br> + Static website hosting configuration
  <br> + Block Public Access settings
  <br> + Public object configuration
  <br> + Website testing

- CloudFront CDN optimization:
  <br> + CloudFront distribution creation
  <br> + Public S3 access blocking
  <br> + CloudFront configuration
  <br> + CloudFront verification

- S3 Advanced Features:
  <br> + Bucket versioning setup and management
  <br> + Object movement between buckets
  <br> + Object replication to different regions