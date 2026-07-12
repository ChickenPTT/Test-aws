---
title: "AWS AI & Cloud Operations Workshop"
date: 2026-06-12
weight: 4
chapter: false
pre: " <b> 4.3. </b> "
---

# B�i thu ho?ch "AWS AI & Cloud Operations Workshop"

### M?c ��ch C?a S? Ki?n

- C?p nh?t xu hu?ng ?ng d?ng AI Agent trong v?n h�nh h? t?ng cloud, DevOps v� x? l� s? c? h? th?ng.
- T�m hi?u c�c b�i to�n th?c t? v? AI Voice, x? l� ti?ng Vi?t, d? tr? ph?n h?i v� tr?i nghi?m h?i tho?i t? nhi�n.
- Kh�m ph� c�ch AI h? tr? doanh nghi?p trong tuy?n d?ng, onboarding, d�nh gi� ?ng vi�n v� t?i uu quy tr�nh nh�n s?.
- Li�n h? ki?n th?c s? ki?n v?i proposal u?c t�nh chi ph� AWS cho h? th?ng serverless x? l� h�ng h�a hu h?ng.

### Danh S�ch Di?n Gi?

- **Truong Tran** � AI Solution Sales, Noventiq
- **Steve Tran** � CTO/Founder, CloudThinker
- **Trung Vu** � CEO, Revve AI
- **Anh Dang** � Solution Sales, Noventiq
- **Nghi Danh** � AI Engineer, Renova Cloud
- **Kiet Tran** � AI Engineer, AWS Student Builder Group
- **Bao Phan** � Cloud Engineer, Cloud Kinetics
- **Nguyen Nguyen** � Cloud Engineer, Cloud Kinetics
- **Toan Nguyen** � AWS Security Builder

---

### N?i Dung N?i B?t

#### AgenticOps for Your Cloud

Di?n gi? **Steve Tran** chia s? v? th?c tr?ng v?n h�nh cloud trong c�c h? th?ng microservices ph?c t?p. Khi log, tracing, metric v� alert b? ph�n t�n ? nhi?u noi, k? su v?n h�nh thu?ng m?t nhi?u th?i gian d? di?u tra nguy�n nh�n g?c r? c?a s? c?.

- **Th?c tr?ng v?n h�nh cloud**: C�c h? th?ng hi?n d?i c� nhi?u th�nh ph?n d?c l?p, l�m cho qu� tr�nh gi�m s�t, truy v?t l?i v� ph?n h?i s? c? tr? n�n kh� khan hon.
- **Gi?i ph�p AgenticOps**: AI Agent du?c d�ng d? t? d?ng h�a c�c bu?c di?u tra, t?ng h?p d? li?u v� d? xu?t hu?ng x? l�, gi�p gi?m th?i gian ph�n t�ch t? h�ng gi? xu?ng c�n v�i ph�t.
- **Quy tr�nh ho?t d?ng**:
  - **Classification**: Ph�n lo?i s? c? t? alert ho?c y�u c?u tr?c ti?p.
  - **Investigation**: Ph�n t�ch log, metric, topology v� gi? thuy?t nguy�n nh�n.
  - **Mitigation**: G?i � phuong �n kh?c ph?c an to�n d? k? su quy?t d?nh.
  - **Optimization**: �? xu?t c?i ti?n d�i h?n nh?m h?n ch? l?i t�i di?n.

#### Gi?ng N�i C?a AI (AI Voice)

Ph?n chia s? c?a **Trung Vu**, **Nghi Danh** v� **Kiet Tran** t?p trung v�o c�ch x�y d?ng tr?i nghi?m h?i tho?i b?ng gi?ng n�i c� d? tr? th?p v� ph� h?p v?i ngu?i d�ng Vi?t Nam.

- **Y�u c?u v? d? tr?**: �? h?i tho?i t? nhi�n, h? th?ng c?n x? l� theo co ch? streaming t? Speech-to-Text, LLM d?n Text-to-Speech, thay v� d?i ngu?i d�ng n�i xong to�n b? c�u l?nh.
- **Th�ch th?c c?a ti?ng Vi?t**: AI c?n hi?u c�ch xung h�, gi?i t�nh, ng? c?nh giao ti?p v� s?c th�i ng�n ng? d? tr�nh ph?n h?i thi?u t? nhi�n ho?c thi?u t�n tr?ng.
- **X? l� gi?ng v�ng mi?n**: D? li?u hu?n luy?n c?n c� t? l? gi?ng v�ng mi?n ph� h?p d? c?i thi?n kh? nang nh?n di?n, nhung v?n c?n ki?m so�t d? AI kh�ng t? d?ng b?t chu?c gi?ng d?a phuong m?t c�ch thi?u chuy�n nghi?p.

#### Kh�a C?nh K? Thu?t V� ?ng D?ng Th?c T? C?a DevOps Agent

C�c di?n gi? minh h?a t�nh hu?ng website b? ch?m ho?c l?i do lu?ng request tang d?t bi?n. Trong h? th?ng truy?n th?ng, k? su ph?i t? truy c?p nhi?u dashboard kh�c nhau d? gom log, tracing v� metric. V?i AI Agent, qu� tr�nh n�y c� th? du?c t? d?ng h�a theo hu?ng c� ki?m so�t.

- **Incident Investigation**: AI Agent t?ng h?p d? li?u quan s�t du?c, t?o topology h? th?ng v� dua ra gi? thuy?t v? nguy�n nh�n g�y l?i.
- **Kh? nang m? r?ng**: Agent c� th? t�ch h?p v?i MCP (Model Context Protocol), Slack, ServiceNow ho?c c�c c�ng c? v?n h�nh kh�c.
- **Luu � b?o m?t**: Agent ch? n�n truy c?p d? li?u du?c c?p quy?n r� r�ng. N?u log chua du?c export ra CloudWatch ho?c h? th?ng quan s�t t?p trung, Agent kh�ng n�n t? � SSH v�o m�y ch? d? l?y d? li?u.
- **Demo th?c t?**: T�nh hu?ng gi? l?p DDoS v?i 1.000 request/gi�y v�o ALB, AI Agent ph�t hi?n 10 ECS Tasks b? spam v� g?i � l?nh d?ng c�c task li�n quan.

#### Case Study Th?c T?

- **M?t tru?ng d?i h?c tr?c tuy?n**: Gi?m MTTR t? 2 ti?ng xu?ng c�n 28 ph�t, tuong duong nhanh hon kho?ng 77%.
- **N?n t?ng c�ng ngh? nh� h�ng Zenchef**: Ph�t hi?n l?i c?u h�nh trong kho?ng 20 ph�t.

#### AI V� Ngu?n Nh�n L?c Trong Doanh Nghi?p

Ph?n tr�nh b�y c?a **Truong Tran** v� **Anh Dang** d? c?p d?n c�ch AI h? tr? b? ph?n HR trong tuy?n d?ng v� v?n h�nh nh�n s?.

- **Gi? ch�n nh�n t�i**: Doanh nghi?p c?n gi?m r?i ro m?t nh�n s? sau qu� tr�nh d�o t?o v� onboarding.
- **��nh gi� ?ng vi�n**: AI h? tr? d?i chi?u CV v?i m� t? c�ng vi?c, ki?m tra k? nang, kinh nghi?m v� m?c d? ph� h?p.
- **T? d?ng h�a onboarding**: R�t ng?n th?i gian nh�n s? m?i h�a nh?p v?i quy tr�nh, t�i li?u v� h? th?ng n?i b?.
- **No-code/Low-code v?i Amazon Q**: HR c� th? x�y d?ng ?ng d?ng qu?n l� tuy?n d?ng ho?c h? tr? ph�n t�ch h? so m� kh�ng c?n l?p tr�nh ph?c t?p.
- **Live demo**: Amazon Q du?c d�ng d? t?o JD cho v? tr� Junior Cloud Engineer, so s�nh nang l?c ?ng vi�n theo k? nang k? thu?t, tu duy gi?i quy?t v?n d?, giao ti?p v� tham kh?o m?c luong ph� h?p.

---

### Nh?ng G� H?c �u?c

#### Tu Duy V?n H�nh Cloud V?i AI Agent

- Hi?u r� AI Agent kh�ng thay th? ho�n to�n k? su v?n h�nh, m� d�ng vai tr� tr? l� ph�n t�ch d? li?u, gom ng? c?nh v� d? xu?t phuong �n x? l�.
- Nh?n ra t?m quan tr?ng c?a observability trong cloud: log, metric, tracing v� alert ph?i du?c thi?t k? t?t th� Agent m?i c� d? li?u d�ng tin c?y d? ph�n t�ch.
- N?m du?c quy tr�nh v?n h�nh s? c? theo c�c bu?c ph�n lo?i, di?u tra, gi?m thi?u t�c d?ng v� t?i uu d�i h?n.

#### K? Thu?t X�y D?ng ?ng D?ng AI Voice

- H?c du?c r?ng tr?i nghi?m AI Voice ph? thu?c r?t l?n v�o latency v� kh? nang streaming li�n t?c gi?a c�c th�nh ph?n.
- Nh?n th?c r� hon v? nh?ng kh� khan ri�ng c?a ti?ng Vi?t nhu c�ch xung h�, gi?ng v�ng mi?n v� ng? c?nh giao ti?p.
- Hi?u r?ng d? li?u hu?n luy?n c?n du?c l?a ch?n c?n th?n d? c�n b?ng gi?a d? ch�nh x�c, t�nh t? nhi�n v� s? chuy�n nghi?p.

#### ?ng D?ng AI Trong Doanh Nghi?p

- AI c� th? gi�p t? d?ng h�a c�c c�ng vi?c l?p l?i trong tuy?n d?ng, ph�n t�ch CV, l�n l?ch ph?ng v?n v� h? tr? onboarding.
- C�c c�ng c? nhu Amazon Q gi�p ngu?i d�ng nghi?p v? t?o ?ng d?ng n?i b? nhanh hon, d?c bi?t trong c�c quy tr�nh c� nhi?u d? li?u v� ti�u ch� d�nh gi�.
- Khi �p d?ng AI v�o doanh nghi?p, c?n ch� � d?n quy?n truy c?p d? li?u, t�nh minh b?ch v� kh? nang ki?m so�t quy?t d?nh cu?i c�ng b?i con ngu?i.

---

### ?ng D?ng V�o Proposal V� D? �n AWS

- **Thi?t k? v?n h�nh cho h? th?ng serverless**: Ki?n th?c v? AgenticOps c� th? �p d?ng v�o h? th?ng ph�t hi?n v� x? l� h�ng h�a hu h?ng tr�n AWS b?ng c�ch chu?n h�a log t? Lambda, API Gateway, SQS, S3, Rekognition, Textract v� DynamoDB v? CloudWatch.
- **T?i uu chi ph� theo hu?ng quan s�t du?c**: Proposal chi ph� AWS cho th?y h? th?ng th? nghi?m v?n n?m trong Free Tier. Tuy nhi�n khi m? r?ng, c?n theo d�i metric s? d?ng theo t?ng d?ch v? d? ki?m so�t chi ph� v� ph�t hi?n b?t thu?ng s?m.
- **Tang d? tin c?y c?a quy tr�nh x? l� ?nh**: AI Agent c� th? h? tr? ki?m tra l?i trong pipeline S3 ? SQS ? Lambda ? Rekognition/Textract ? DynamoDB, d?c bi?t khi ?nh x? l� th?t b?i ho?c d? tin c?y AI th?p.
- **C?i thi?n tr?i nghi?m ngu?i d�ng**: Ki?n th?c AI Voice c� th? m? r?ng cho ch?c nang nh?p th�ng tin b?ng gi?ng n�i trong tuong lai, gi�p nh�n vi�n kho b�o c�o t�nh tr?ng h�ng h�a nhanh hon.

---

### Tr?i Nghi?m Trong S? Ki?n

S? ki?n mang l?i g�c nh�n th?c t? v? c�ch AI dang du?c dua v�o v?n h�nh cloud, DevOps v� quy tr�nh doanh nghi?p. �i?m d�ng ch� � l� c�c ph?n tr�nh b�y kh�ng ch? n�i v? � tu?ng AI t?ng qu�t, m� di s�u v�o c�c t�nh hu?ng c� th? �p d?ng ngay nhu di?u tra s? c?, ph�n t�ch log, gi?m MTTR, x? l� gi?ng n�i ti?ng Vi?t v� t? d?ng h�a tuy?n d?ng.

- **Kh�ng gian h?c h?i th?c t?**: Ngu?i tham gia du?c nghe c�c case study c? th? t? cloud operations, AI Voice v� HR automation.
- **G�c nh�n k? thu?t r� r�ng**: C�c di?n gi? gi?i th�ch c�ch AI Agent ph?i h?p v?i telemetry, MCP, CloudWatch v� c�c c�ng c? v?n h�nh d? h? tr? k? su.
- **Li�n h? t?t v?i d? �n c� nh�n**: N?i dung s? ki?n gi�p c?ng c? c�ch thi?t k? h? th?ng AWS kh�ng ch? ch?y du?c, m� c�n c?n d? quan s�t, d? ki?m so�t chi ph� v� d? x? l� s? c?.

#### M?t s? h�nh ?nh khi tham gia s? ki?n

<div style="display: flex; gap: 10px; justify-content: center; flex-wrap: wrap;">
  <img src="/images/4-Events-Participated/Image_event/event2-1.png" alt="AWS AI and Cloud Operations Workshop 1" width="45%" />
  <img src="/images/4-Events-Participated/Image_event/event2-2.png" alt="AWS AI and Cloud Operations Workshop 2" width="45%" />
</div>
