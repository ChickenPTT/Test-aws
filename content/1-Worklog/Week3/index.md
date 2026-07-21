---
title: "Worklog Week 3"
date: 2026-05-18
weight: 3
chapter: false
pre: ""
---

### Week 3 Objectives:

- Gain a solid foundational understanding of Amazon Relational Database Service (Amazon RDS) and its database management features
- Practice creating and configuring an RDS database instance on AWS
- Understand how to set up VPC, Security Groups, and DB Subnet Groups for RDS
- Practice Backup and Restore operations on RDS
- Get familiar with Amazon Lightsail for deploying lightweight, cost-effective applications
- Understand how to deploy applications on Lightsail (WordPress, PrestaShop, Akaunting)
- Grasp the concepts of Lightsail management features such as Snapshots, instance scaling, and monitoring

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | Start Date | Completion Date | Reference Source                                       |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------ |
| 2   | **Hands-on lab: Creating a database on Amazon Relational Database Service (Amazon RDS)** <br>&emsp; + Overview and introduction <br>&emsp; + Preparation steps: <br>&emsp;&emsp; • Create a VPC <br>&emsp;&emsp; • Create an EC2 security group <br>&emsp;&emsp; • Create an RDS subnet group <br>&emsp;&emsp; • Create a DB Subnet group <br>&emsp; + Create an EC2 instance <br>&emsp; + Create an RDS database instance <br>&emsp; + Deploy the application <br>&emsp; + Backup and restore                                                                                                                                                                                                                                                                                                                                                                                                                                              | 05/18/2026   | 05/18/2026      | <https://000005.awsstudygroup.com/vi/>                 |
| 3   | **Hands-on lab: Optimizing computing costs with Amazon Lightsail** <br>&emsp; + Overview and introduction <br>&emsp; + Deploy a Lightsail database <br>&emsp; + Deploy a WordPress Instance: <br>&emsp;&emsp; • Deploy the instance <br>&emsp;&emsp; • Configure Ubuntu <br>&emsp;&emsp; • Configure Networking <br>&emsp;&emsp; • Configure WordPress <br>&emsp; + Deploy a PrestaShop E-Commerce Instance: <br>&emsp;&emsp; • Deploy the instance <br>&emsp;&emsp; • Configure Networking <br>&emsp;&emsp; • Deploy the application <br>&emsp; + Deploy an Akaunting Instance: <br>&emsp;&emsp; • Deploy the instance <br>&emsp;&emsp; • Configure networking <br>&emsp;&emsp; • Deploy the application <br>&emsp; + Secure the application <br>&emsp; + Create a Snapshot <br>&emsp; + Switch to a larger instance as application resource usage increases <br>&emsp; + Set up alerts for high CPU resource usage | 05/19/2026   | 05/20/2026      | <https://000045.awsstudygroup.com/vi/8-create-alarms/> |
| 4   | **Hands-on lab: Automatically scaling an application with Amazon EC2 Autoscaling** <br>&emsp; + Overview and benefits of an Auto Scaling Group <br>&emsp; + Introduction to Auto Scaling Group <br>&emsp; + Preparation steps: <br>&emsp;&emsp; • Set up the network infrastructure <br>&emsp;&emsp; • Initialize the EC2 instance <br>&emsp;&emsp; • Initialize a Database instance with RDS <br>&emsp;&emsp; • Install the database data <br>&emsp;&emsp; • Deploy the web server <br>&emsp;&emsp; • Prepare metrics for Predictive Scaling <br>&emsp;&emsp; • Create a Launch Template                                                                                                                                                                                                                                                                                                                                              | 05/20/2026   | 05/20/2026      | <https://000006.awsstudygroup.com/vi/1-introduction/>  |
| 5   | **Continued hands-on lab: Automatically scaling an application with Amazon EC2 Autoscaling** <br>&emsp; + Set up the load balancer <br>&emsp; + Check the results <br>&emsp; + Create an auto scaling group <br>&emsp; + Test the solutions: <br>&emsp;&emsp; • Manual scaling <br>&emsp;&emsp; • Scheduled scaling <br>&emsp;&emsp; • Dynamic scaling <br>&emsp;&emsp; • Predictive scaling <br>&emsp; + Review the Autoscaling lab                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | 05/21/2026   | 05/21/2026      | <https://000006.awsstudygroup.com/vi/1-introduction/>  |

### Week 3 Results Achieved

**RDS Core Knowledge:**

- Basic understanding of RDS concepts:
  <br> + Overview of Amazon RDS
  <br> + VPC setup and configuration
  <br> + EC2 Security Groups configuration for RDS
  <br> + RDS Subnet Groups
  <br> + DB Subnet Groups
  <br> + EC2 Instance setup

- Deploying an RDS Database:
  <br> + RDS database instance creation
  <br> + Database configuration and setup
  <br> + Application deployment on RDS
  <br> + Backup and Restore operations
  <br> + Data management and recovery

**Amazon Lightsail Overview:**

- Basic understanding of Amazon Lightsail concepts:
  <br> + Lightsail overview and introduction
  <br> + Cost-effective solutions
  <br> + Lightsail database setup

**Lightsail Application Deployment:**

- Deploying applications on Lightsail:
  <br> + WordPress Instance:
  <br>&emsp;&emsp; • Instance deployment
  <br>&emsp;&emsp; • Ubuntu configuration
  <br>&emsp;&emsp; • Networking setup
  <br>&emsp;&emsp; • WordPress configuration
  <br> + PrestaShop E-Commerce Instance:
  <br>&emsp;&emsp; • Instance deployment
  <br>&emsp;&emsp; • Networking configuration
  <br>&emsp;&emsp; • Application deployment
  <br> + Akaunting Instance:
  <br>&emsp;&emsp; • Instance deployment
  <br>&emsp;&emsp; • Networking configuration
  <br>&emsp;&emsp; • Application deployment
  <br>&emsp;&emsp; • Application security

**Lightsail Management and Optimization:**

- Managing and optimizing Lightsail instances:
  <br> + Snapshot creation and management
  <br> + Instance scaling as resources increase
  <br> + CPU resource monitoring
  <br> + Alert configuration for resource usage
  <br> + Automatic scaling based on resource consumption

**Optimizing Computing Costs with Amazon Lightsail**

- Securing the application
- Creating a Snapshot
- Switching to a larger instance as application resource usage increases
- Setting up alerts for high CPU resource usage

**Automatically Scaling an Application with Amazon EC2 Autoscaling**

- Overview and benefits of an Auto Scaling Group
- Introduction to Auto Scaling Group
- Preparation steps:
  <br> + Setting up the network infrastructure
  <br> + Initializing the EC2 instance
  <br> + Initializing a Database instance with RDS
  <br> + Installing the database data
  <br> + Deploying the web server
  <br> + Preparing metrics for Predictive Scaling
  <br> + Creating a Launch Template