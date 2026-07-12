---
title: "T?o v� vi?t code cho AWS Lambda"
date: 2026-06-21
weight: 5
chapter: false
pre: ""
---

# Bu?c 4: T?o v� vi?t code cho AWS Lambda

### M?c ti�u

Trong bu?c n�y, b?n s? t?o Lambda Function d? nh?n message t? Amazon SQS, d?c th�ng tin ?nh du?c upload l�n Amazon S3 v� g?i c�c d?ch v? AI nhu Amazon Rekognition v� Amazon Textract d? ph�n t�ch ?nh.

---

### 4.1 - T?o Lambda Function

1. Truy c?p **AWS Lambda**, ch?n **Create function**.

![Truy c?p AWS Lambda](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image1.png)

2. Ch?n **Author from scratch**.

![Ch?n Author from scratch](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image2.png)

![T?o Lambda function](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image3.png)

3. C?u h�nh Lambda Function.

![C?u h�nh Lambda function](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image4.png)

![Ch?n runtime v� role](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image5.png)

G?i � c?u h�nh:

- Function name: **image-quality-processor**
- Runtime: **Python 3.x**
- Execution role: ch?n IAM Role **Lambda-ImageProcessing-Role** d� t?o ? bu?c 1

4. Ch?n **Create function**.

![Create function](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image6.png)

5. V�o tab **Configuration**, ch?n **General configuration**, sau d� ch?n **Edit**.

![M? General configuration](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image7.png)

6. �?t **Timeout = 60 gi�y**, sau d� luu c?u h�nh.

![�?t timeout cho Lambda](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image8.png)

---

### 4.2 - G?n SQS l�m Trigger

1. ? trang Lambda Function, ch?n **Add trigger**.

![Add trigger cho Lambda](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image9.png)

2. Ch?n source l� **SQS**.

![Ch?n SQS trigger](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image10.png)

3. Ch?n queue **image-processing-queue**.

4. C?u h�nh **Batch size = 1**.

Batch size b?ng 1 gi�p Lambda x? l� t?ng message m?t, ph� h?p cho lab v� d? quan s�t log v� debug.

5. Ch?n **Add**.

![C?u h�nh SQS trigger](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image11.png)

---

### 4.3 - Vi?t code Python

1. V�o tab **Code**.

2. X�a code m?u, d�n do?n code Python x? l� SQS message, sau d� ch?n **Deploy** d? luu code.

![Vi?t code Lambda v� Deploy](/images/5-Workshop/5.CreateAndCode-LambdaFunction/images/image12.png)

Code m?u:

```python
import json
import urllib.parse

import boto3

s3 = boto3.client("s3")
rekognition = boto3.client("rekognition")
textract = boto3.client("textract")


def lambda_handler(event, context):
    for record in event["Records"]:
        body = json.loads(record["body"])

        for s3_record in body.get("Records", []):
            bucket = s3_record["s3"]["bucket"]["name"]
            key = urllib.parse.unquote_plus(s3_record["s3"]["object"]["key"])

            print(f"Processing image: s3://{bucket}/{key}")

            labels = rekognition.detect_labels(
                Image={
                    "S3Object": {
                        "Bucket": bucket,
                        "Name": key
                    }
                },
                MaxLabels=10,
                MinConfidence=70
            )

            print("Rekognition labels:")
            for label in labels["Labels"]:
                print(f"- {label['Name']}: {label['Confidence']:.2f}%")

            text_result = textract.detect_document_text(
                Document={
                    "S3Object": {
                        "Bucket": bucket,
                        "Name": key
                    }
                }
            )

            print("Textract text:")
            for block in text_result["Blocks"]:
                if block["BlockType"] == "LINE":
                    print(block["Text"])

    return {
        "statusCode": 200,
        "body": "Processed SQS messages successfully"
    }
```
