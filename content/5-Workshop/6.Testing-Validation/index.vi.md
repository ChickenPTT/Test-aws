---
title: "Ki?m th? h? th?ng"
date: 2026-06-21
weight: 6
chapter: false
pre: ""
---

# Bu?c 5: Ki?m th? h? th?ng

### M?c ti�u

X�c nh?n to�n b? lu?ng **S3 -> SQS -> Lambda -> AI** ho?t d?ng d�ng.

Trong bu?c n�y, b?n s? upload ?nh l�n S3, ki?m tra Lambda x? l� message t? SQS v� xem k?t qu? ph�n t�ch trong CloudWatch Logs.

---

### 5.1 - Chu?n b? ?nh test

Chu?n b? �t nh?t 2 lo?i ?nh:

- ?nh ki?n h�ng b? m�p ho?c r�ch d? ki?m tra Amazon Rekognition ph�t hi?n d�ng n?i dung ?nh.
- ?nh c� nh�n d�n v?i m� v?n don r� r�ng d? ki?m tra Amazon Textract tr�ch xu?t d�ng van b?n.

---

### 5.2 - T?i ?nh l�n S3

1. V�o S3 bucket **logistics-raw-images-&lt;t�n-b?n&gt;**, sau d� ch?n **Upload**.

2. T?i l�n kho?ng **5-10 ?nh** c�ng l�c d? ki?m tra kh? nang x? l� song song.

3. Ch?n **Upload** d? b?t d?u t?i ?nh.

![Upload ?nh l�n S3](/images/5-Workshop/6.Testing-Validation/images/image13.png)

![Ho�n t?t upload ?nh](/images/5-Workshop/6.Testing-Validation/images/image14.png)

---

### 5.3 - Ki?m tra CloudWatch Logs

1. Truy c?p **CloudWatch**, ch?n **Log groups**.

2. T�m log group **/aws/lambda/image-quality-processor**.

3. Ch?n log stream m?i nh?t v� ki?m tra output t? Lambda.

![Ki?m tra CloudWatch Log groups](/images/5-Workshop/6.Testing-Validation/images/image15.png)

![Ki?m tra output Lambda](/images/5-Workshop/6.Testing-Validation/images/image16.png)

---

### 5.4 - Ki?m tra SQS d� x? l� s?ch

1. V�o **SQS Console**, ch?n queue **image-processing-queue**.

2. Ch?n **Send and receive messages**.

3. Ch?n **Poll for messages**.

N?u queue tr?ng, nghia l� Lambda d� x? l� h?t to�n b? tin nh?n th�nh c�ng.

![Ki?m tra message trong SQS](/images/5-Workshop/6.Testing-Validation/images/image17.png)
