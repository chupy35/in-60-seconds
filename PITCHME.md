---?color=black
### Modeling and Simulating Software Architectures with Palladio
&nbsp;
@box[bg-orange text-white demo-box-text-padding rounded](Workload-Aware Monitoring of a 1&1 E-mail System)

---?color=black
#### @color[white](**Predicting Performance Quality in Distributed Systems**)

![](template/img/palladioperf.png)

---?color=black
@title[Goals and Questions]

@snap[north-west text-white]
Goals and Questions
@snapend

@snap[south-west list-content-concise span-100 text-white ]
@ol
- How to integrate model-based predictions into the run-time monitoring of systems?
- How to model a large and distributed system consisting of several hundred servers?
- How to calibrate the prediction model only on the basis of existing run-time monitoring data without running experiments? 
@olend
<br><br>
@snapend

---?image=template/img/bg/black.jpg&position=right&size=50% 100%
@title[Text + Image]

@snap[east span-50 text-white text-05]
@ul[split-screen-list text-09 span-90](false)
**System Description**

&nbsp;

- One of the biggest hosters and leading domain registrars
- Backend: E-mail sending, receiving requests, persistence via restful HTTP services, POP3, or IMAP
- Service oriented paradigm
- Individual deployment per component on dedicated servers in redundant instances.
@ulend
@snapend

@snap[west]
@img[split-screen-img span-50](template/img/img1.png)
@snapend

---?image=template/img/bg/black.jpg&position=right&size=50% 100%
@title[Text + Image]

@snap[east span-50 text-white text-05]
@ul[split-screen-list text-09 span-90](false)
- STORE: folder structures of mailboxes and attachments are saved
- SERIE and DBFM db: fast access to internal instances informations which single mailboxes are dedicated
- Mail Delivery Agents (MDAs) and mail transfer agents (MTAs): located on mail exchanger (MX) and mail proxy (MP) servers)
- External clients connect to the proxy with IMAP and POP3 requests and forward requests to the STORE servers
- Clients use Restful api
- More components added like antivirus and other tasks
@ulend
@snapend

@snap[west]
@img[split-screen-img span-50](template/img/img1.png)

---?image=template/img/bg/orange.jpg&position=right&size=50% 100%
@title[Heading + List Body]

@snap[west text-16 text-bold text-italic text-orange span-50]
Modeling
@snapend

@snap[west]
@img[split-screen-img span-50](template/img/img2.png)

@snap[east text-white span-45]
@ol[split-screen-list text-06](false)
**Modeling - Workload-aware Performance Montoring**

&nbsp;

- Main activities: Model preparation, Model calibration and prediction and comparison 
- Model has to be specified only once
- 1st activity: Model describing the system 
- 2nd activity: Available hardware resources are described 
@olend
@snapend

---?color=black

@snap[west span-40]
# Analysis
@snapend

@snap[north-east span-40 fragment text-06]
@box[bg-purple text-white](.#Prediction of expected resource utilization requires measuring the current workload.)
@snapend

@snap[east span-40 fragment text-06]
@box[bg-orange text-white](.#Prediction model is completed with the specification of system's usage within the Usage Model generation.)
@snapend

@snap[south-east span-40 fragment text-06]]
@box[bg-pink text-white](.#The resulting Usage-Model is used as an input to the performance prediction, after collecting performance metrics and the prediction, they are analyzed and compared)@snapend

---?color=#8ea33a
@title[Application of the Workload-Aware Performance Monitoring Process In the following, we present the application of our approach in the industrial context]

@snap[north-west]
#### @color[white](**Store subsystem**)
@snapend

@snap[west span-50]
@ul[spaced text-white text-05]
- SGATE component handles internal requests from other components (Proxy - Store communication)
- For availability and prevent data loss Store server run as a cluster of two servers
- Each clients mailbox is associated with one server
- In case of failure the other server takes responsibility and the backup is for persistency
- Distributed Load
- SGATE, IMAP and POP3 -> 10 servers
- BACKUP -> 22 servers
@ulend
@snapend

@snap[east span-45]
@img[shadow](template/img/img3.png)
@snapend

---?image=template/img/bg/green.jpg&position=left&size=50% 100%
@title[Performance Modeling Study]

@snap[north-west span-50]
###### @color[white](**Performance Modeling Study**)
@snapend

@snap[west span-50]
@ul[spaced text-white text-05]
- SGATE component handles internal requests from other components (Proxy - Store communication)
- For availability and prevent data loss Store server run as a cluster of two servers
- Each clients mailbox is associated with one server
- In case of failure the other server takes responsibility and the backup is for persistency
- Distributed Load
- SGATE, IMAP and POP3 -> 10 servers
- BACKUP -> 22 servers
@ulend
@snapend

@snap[east fragment]
@img[split-screen-img span-55](template/img/developer.jpg)
@snapend

@snap[south-west template-note text-white]
Split-screen text and image-fragment template.
@snapend
