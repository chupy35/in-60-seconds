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
@ul[split-screen-list text-07 span-80](false)
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
@ul[split-screen-list text-07](false)
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
