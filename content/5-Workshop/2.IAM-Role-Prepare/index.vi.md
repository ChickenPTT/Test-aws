---
title: "Chu?n b? IAM Role cho Lambda"
date: 2026-06-21
weight: 2
chapter: false
pre: ""
---

# Bu?c 1: Chu?n b? IAM Role cho Lambda

### Gi?i thi?u

IAM Role l� quy?n m� Lambda s? d?ng d? truy c?p c�c d?ch v? AWS c?n thi?t trong workshop nhu Amazon S3, Amazon SQS, Amazon Rekognition v� Amazon Textract.

Trong bu?c n�y, b?n s? t?o m?t IAM Role cho Lambda v� g?n c�c policy c?n thi?t d? Lambda c� th? d?c d? li?u, nh?n message v� ghi log trong qu� tr�nh x? l� ?nh.

---

### C�c bu?c th?c hi?n

1. Truy c?p **AWS Console**, t�m d?ch v? **IAM**.

![T�m d?ch v? IAM](/images/5-Workshop/2.IAM-Role-Prepare/images/image1.png)

2. Ch?n **Roles**, sau d� ch?n **Create role**.

![Ch?n Roles v� Create role](/images/5-Workshop/2.IAM-Role-Prepare/images/image2.png)

3. ? ph?n **Trusted entity type**, ch?n **AWS service**.

4. ? ph?n **Use case**, ch?n **Lambda**, sau d� ch?n **Next**.

![Ch?n AWS service v� Lambda](/images/5-Workshop/2.IAM-Role-Prepare/images/image3.png)

5. T�m v� g?n l?n lu?t c�c policy c?n thi?t cho Lambda.

![T�m policy cho Lambda](/images/5-Workshop/2.IAM-Role-Prepare/images/image4.png)

![Ch?n policy cho Lambda](/images/5-Workshop/2.IAM-Role-Prepare/images/image5.png)

![G?n policy AWSLambdaBasicExecutionRole](/images/5-Workshop/2.IAM-Role-Prepare/images/image6.png)

![G?n policy AmazonS3ReadOnlyAccess](/images/5-Workshop/2.IAM-Role-Prepare/images/image7.png)

![G?n policy AmazonSQSFullAccess](/images/5-Workshop/2.IAM-Role-Prepare/images/image8.png)

![G?n policy Rekognition v� Textract](/images/5-Workshop/2.IAM-Role-Prepare/images/image9.png)

6. �?t t�n role l� **Lambda-ImageProcessing-Role**, sau d� ch?n **Create role**.

![�?t t�n IAM Role](/images/5-Workshop/2.IAM-Role-Prepare/images/image10.png)

![T?o IAM Role](/images/5-Workshop/2.IAM-Role-Prepare/images/image11.png)

---

### Luu � b?o m?t

Trong m�i tru?ng th?c t?, thay v� d�ng policy c� s?n c?a AWS, b?n n�n t? vi?t **Custom Policy** d? gi?i h?n quy?n ch? tr�n d�ng bucket ho?c queue c? th?.

��y l� best practice b?o m?t theo nguy�n t?c **Least Privilege**, t?c l� ch? c?p d�ng quy?n c?n thi?t v� kh�ng c?p du quy?n.

![Custom policy theo nguy�n t?c Least Privilege](/images/5-Workshop/2.IAM-Role-Prepare/images/image12.png)
