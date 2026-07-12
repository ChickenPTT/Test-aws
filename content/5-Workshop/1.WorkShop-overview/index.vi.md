---
title: "T?ng quan v? Workshop"
date: 2026-06-21
weight: 1
chapter: false
pre: ""
---

# X�y d?ng lu?ng x? l� h�nh ?nh b?t d?ng b? s? d?ng Amazon S3, SQS v� AWS Lambda

### T�m t?t v? workshop

Workshop n�y hu?ng d?n b?n x�y d?ng m?t lu?ng x? l� ?nh b?t d?ng b? (asynchronous) theo m� h�nh Event-Driven tr�n AWS, gi?i quy?t b�i to�n �nhi?u ngu?i d�ng upload ?nh c�ng l�c� nhung v?n d?m b?o h? th?ng ?n d?nh, d? m? r?ng v� ki?m so�t chi ph�.

---

### M?c ti�u ch�nh

- Thi?t k? ki?n tr�c **S3 ? SQS ? Lambda** d? x? l� ?nh theo h�ng d?i, tr�nh Lambda b? g?i ? ?t khi c� nhi?u upload d?ng th?i.
- Vi?t Lambda (Python) d?:
    - Nh?n message t? SQS (ch?a s? ki?n t? S3)
    - T?i ?nh t? S3
    - G?i Amazon Rekognition d? g?i � nh�n/nh?n di?n t�nh tr?ng (v� d?: ki?n h�ng hu h?ng)
    - G?i Amazon Textract d? tr�ch xu?t van b?n tr�n nh�n d�n (m� v?n don, th�ng tin tuy?n, S�T, �)
    - Ghi k?t qu? ra CloudWatch Logs d? quan s�t v� ki?m th?
### B?n s? h?c du?c g�
- V� sao c?n SQS l�m �buffer� gi?a S3 v� Lambda trong h? th?ng c� t?i cao.
- C�ch c?u h�nh IAM Role theo nguy�n t?c Least Privilege (c?p d�ng quy?n c?n thi?t).
- C�ch t?o & c?u h�nh:
    - S3 bucket v� Event Notification
    - SQS Standard Queue v?i c�c th�ng s? quan tr?ng (Visibility Timeout, retention�)
    - Lambda Trigger t? SQS v� x? l� t?ng message (batch size nh? d? d? quan s�t)
- Quy tr�nh Testing & Validation end-to-end v� Clean up t�i nguy�n d? tr�nh ph�t sinh chi ph�.