Download Link: https://assignmentchef.com/product/solved-comp90073-assignment1-detecting-cyberattacks-in-network-traffic-data
<br>
In this Project, you are given a network traffic data and should use Splunk to identify cyberattacks by leveraging the analytics capabilities of this software. The aim is to strengthen your skills in analyzing traffic patterns and identifying their changes over time, which might be signs of suspicious activities. In searching the evidences of cyberattacks, and hunting the attack sources and targets, you will develop the practical security incident investigation skills and mindset of a real-world Cyber Security Analyst. In addition, you will skill-up yourself in tracing attacks back in time to create an attack narrative<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>. Then generating and extracting significant patterns/features of detected attacks will pave the way for the next project that is heavily machine learning focused. Lastly, you will develop your skills as a Cyber Defender by proposing the countermeasures to detect/mitigate similar attacks in the future.

You will write a technical report on your findings, and your proposal on how the identified attack patterns and evidence can be used to detect and mitigate similar cyberattacks in future.

<h1>Deliverables</h1>

A technical report that describes your methodology for

<ol>

 <li>Ingesting the given pcap file into Splunk</li>

</ol>

<strong><em>Note:</em></strong><em> If you fail to ingest pcap file after multiple attempts, you can ask your Tutor for a copy of the indexed file “&lt;file_name&gt;.pcap.csv”. Then copy the file to this directory: </em>

<em>“$SPLUNK_HOME/etc/apps/SplunkForPCAP/PCAPcsv/”. Please use this as last resort only.  Before asking for the indexed file, please be prepared to lose the mark for this deliverable, and you will have to explain what steps you’ve taken to troubleshoot the issue.   </em>

<ol start="2">

 <li>Analyzing the data using Splunk, validating the evidences of the following attack scenarios contained in the given pcap file. You can use either Splunk Search or PCAP Analyzer Dashboard where applicable, new field extraction may be required if you are using Splunk Search.</li>

</ol>

2.1 Botnet Command &amp; Control (C2)




<ol>

 <li>Calculate the number of HTTP based C2 requests to C2 server “<em>com”</em>, and the URI strings were used (Hint: you will need to get the IP address of the C2 server first)</li>

 <li>List the start time and the end time</li>

</ol>

2.2 SPAM

<ol>

 <li>Calculate how many email addresses have been targeted by this spam (Hint: search by protocol and key word “RCPT”)</li>

 <li>List the start time and the end time, the first and last recipient (email address) of this email spam</li>

</ol>

2.3 ClickFraud

<ol>

 <li>Calculate the number of ClickFraud requests have been made to web site “<em>generalamuse.com”</em>, and the URI strings were used (Hint: you will need to get the IP address of the web site first)</li>

 <li>List the start time and the end time</li>

</ol>

2.4 IRC

<ol>

 <li>Identify all IRC servers (IP addresses) and the number of POST requests made by the infected machine. (Hint: search by protocol or port number)</li>

 <li>List the start and end time</li>

</ol>

<ol start="3">

 <li>Creating the attack narratives using the four scenarios above, please include the IP address of the infected system</li>

 <li>Evaluating the consequences of the attacks on the targeted network (Hint: targeted network is where the infected system belongs to, evaluate the impact using CIA triad)</li>

 <li>Generating and extracting the significant patterns/features for attack scenarios above, <em>g.,</em> “<em>src_IP+dst_IP+dst_Port</em>” is a significant pattern to detect Port Scan</li>

 <li>Assuming you are the Cybersecurity Analyst who is part of the Incident Response team, and you’ve been given the greenlight to put in any controls to mitigate this attack. You can safely ignore any business impact as the priority is to the contain the current attack. Please propose your countermeasures to detect/mitigate the above attacks scenarios, using evidence and patterns in deliverable #<strong><em>2</em></strong> and #<strong><em>5</em></strong></li>

</ol>

<h1>Technical Report</h1>

A technical report, of 2000-2500 words in PDF format, comprising:

<ol>

 <li>A data description and a summary of detected attacks, including the IP addresses of attackers and victims, the attacked services, the timestamp, and the type of the attack per attack scenario.</li>

 <li>Methodology of analysis to find evidence of cyberattacks in the network traffic data.</li>

 <li>Description of each attack and the attack narrative.</li>

 <li>Possible approaches for extracting features (fields) and summary of your approach.</li>

 <li>Proposed countermeasures per attack scenarios.</li>

 <li>Conclusions</li>

</ol>

You should include a bibliography and citations to relevant research papers and external resources and codes you have used.

<h1>Assessment Criteria</h1>

Report (20 marks out of 20)

<ol>

 <li>Methodology: (8 marks)</li>

</ol>

You will describe your methodology in a manner that would make your work reproducible. You should describe in detail how you have detected the cyberattacks using Splunk search capabilities: the exact SPL commands you ran and the corresponding generated results, or the dashboards you used in pcap app (<em>PCAP Analyzer)</em> and the corresponding data and generated results. Your approach to model patterns in data and detect changes in them for identifying cyberattacks should be clearly explained. The description of your proposed countermeasures should include reasons for choosing it based on the types of attacks you have detected. You should not use a network traffic feature generator as a black box without explaining the reasons for extracting the reported features.

<ol start="2">

 <li>Critical Analysis: (6 marks)</li>

</ol>

You should validate the evidence you have found in the data for proving that a certain type of attack has happened. The attack narrative should specify the time of start and end of the attack and the consequences of the attack on the victim network.<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a> You should identify other types of data that could be collected to more accurately and effectively detect/mitigate the identified cyberattacks.

<ol start="3">

 <li>Report Quality: (6 marks)</li>

</ol>

You will produce a formal report and express your methodology and findings concisely and clearly. The quality and description of figures and tables should be acceptable. In real-world scenarios, this report will have a range of audience in a company. Thus, it should be structured such that summary of the findings is available for the managers and non-technical audience and on the other hand, the attack narratives should include technical details for other analyzers that may read your report.

<h1>Description of the Data</h1>

The dataset for Project 1 <a href="https://cloudstor.aarnet.edu.au/plus/s/btftq1LbvFIJF5U">(</a><a href="https://cloudstor.aarnet.edu.au/plus/s/btftq1LbvFIJF5U">download link</a><a href="https://cloudstor.aarnet.edu.au/plus/s/btftq1LbvFIJF5U">)</a> includes packet capture (pcap) file of network traffic for a network that was victim of cyberattacks.  This file was captured on the interfaces of virtual machines being infected by malware, which contains attacks including but not limited to four scenarios listed in the Deliverable section.  It also contains normal traffic prior to malware infection.  This enables you to compare the patterns in data from normal operation (before infection) and post infection to identify attacks that occurred.







<h1>Changes/Updates to the Project Specifications</h1>

If we require any changes or clarifications to the project specifications, they will be posted on the LMS. Any addendums will supersede information included in this document.

<a href="#_ftnref1" name="_ftn1">[1]</a> When the attack was started, the attacker(s), the victim(s) and the type of attack.

<a href="#_ftnref2" name="_ftn2">[2]</a> We validate your findings with our ground truth, and you lose marks for identifying non-anomalous traffic as anomaly and vice-versa.