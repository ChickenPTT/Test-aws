---
title: "C?u h�nh luu tr? v� s? ki?n Amazon S3"
date: 2026-06-21
weight: 4
chapter: false
pre: ""
---

# Bu?c 3: C?u h�nh luu tr? v� s? ki?n Amazon S3

### M?c ti�u

Trong bu?c n�y, b?n s? t?o S3 bucket d? luu ?nh v� c?u h�nh d? m?i khi c� ?nh m?i du?c t?i l�n, Amazon S3 t? d?ng g?i th�ng b�o v�o SQS queue d� t?o ? bu?c tru?c.

---

### 3.1 - T?o S3 Bucket

1. Truy c?p **Amazon S3**, sau d� ch?n **Create bucket**.

![T?o S3 bucket](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image19.png)

2. �?t t�n bucket theo d?nh d?ng **logistics-raw-images-&lt;t�n-b?n&gt;**.

T�n bucket ph?i l� duy nh?t tr�n to�n b? AWS.

![�?t t�n S3 bucket](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image20.png)

3. Ch?n Region **ap-southeast-1 (Singapore)** d? g?n Vi?t Nam.

![Ch?n Region Singapore](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image21.png)

4. Gi? nguy�n c�c c�i d?t m?c d?nh, sau d� ch?n **Create bucket**.

![Gi? c�i d?t m?c d?nh](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image22.png)

![T?o bucket th�nh c�ng](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image23.png)

---

### 3.2 - C?p quy?n cho S3 g?i th�ng b�o v�o SQS

1. V�o **SQS Console**, ch?n queue **image-processing-queue**.

2. M? tab **Access policy**, ch?n ch?nh s?a policy.

3. Th�m policy cho ph�p S3 g?i message v�o SQS.

![M? Access policy c?a SQS](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image24.png)

V� d? policy:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": {
        "Service": "s3.amazonaws.com"
      },
      "Action": "sqs:SendMessage",
      "Resource": "arn:aws:sqs:ap-southeast-1:<account-id>:image-processing-queue",
      "Condition": {
        "ArnLike": {
          "aws:SourceArn": "arn:aws:s3:::logistics-raw-images-<ten-ban>"
        }
      }
    }
  ]
}
```

Thay **&lt;account-id&gt;** b?ng AWS Account ID c?a b?n v� thay **logistics-raw-images-&lt;ten-ban&gt;** b?ng t�n bucket d� t?o.

![Th�m policy cho S3 g?i message v�o SQS](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image25.png)

---

### 3.3 - C?u h�nh S3 Event Notification

1. V�o bucket v?a t?o, m? tab **Properties**, k�o xu?ng ph?n **Event notifications**, sau d� ch?n **Create event notification**.

![M? Event notifications](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image26.png)

![Create event notification](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image27.png)

2. �?t t�n event l� **new-image-uploaded**.

![�?t t�n event notification](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image28.png)

3. ? ph?n **Event types**, t�ch ch?n **s3:ObjectCreated:***.

![Ch?n event type ObjectCreated](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image29.png)

4. ? ph?n **Prefix/Suffix**, nh?p c�c suffix ?nh nhu **.jpg**, **.jpeg**, **.png** d? ch? k�ch ho?t khi c� ?nh t?i l�n.

C?u h�nh n�y gi�p b? qua c�c file kh�ng ph?i ?nh nhu `.txt` ho?c `.pdf`.

![C?u h�nh suffix file ?nh](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image30.png)

5. ? ph?n **Destination**, ch?n **SQS Queue**, sau d� ch?n queue **image-processing-queue**.

![Ch?n SQS queue l�m destination](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image31.png)

6. Ch?n **Save changes** d? luu c?u h�nh.

![Luu event notification](/images/5-Workshop/4.Congif-Save-And-Event(AWS-S3)/images/image32.png)
