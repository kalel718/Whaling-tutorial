<h1>Whaling Email Tutorial</h1>
<img src="https://i.imgur.com/sixEjDy.png" height="80%" width="80%" alt=/>

<h2>Description</h2>
Robert receives an email from Better Business Bureau, claiming his company violating the Fair Labor Standards Act.  Encouraging him to click on a link to see the complaint. Being security conscious, he normally does not click on links. However, this email calls him by name and claims to be a valid source. Which of the following best describes this attack?


 -  <b>A. ClickJacking</b>
 -  B. Spear phishing
 -  C. Social Engineering
 -  D. Whaling

 -  Answer is
 -  D. This is a classic example of whaling, phishing that targets a specific individual.

   <h2>Tutorial walk-through:</h2>


<h2>Here’s a detailed breakdown of how I would handle this alert as a SOC analyst:</h2>

 <b>Initial Alert and Identification
Tool Used: Email Security Gateway (e.g., Proofpoint, Mimecast)
- Action: Identify the suspicious email and flag it for further investigation. Check if similar emails have been reported by other employees.

 <img src="https://i.imgur.com/xfjwOsu.png" height="80%" width="80%" alt=/>


 </b> 2. Analyze the URL
 When submitting the URL to a tool like VirusTotal or URLscan.io, you can capture screenshots of the submission process and the resulting analysis report.
-  Tools: Web browser showing the analysis on VirusTotal or URLscan.io.

   <img src="https://i.imgur.com/vDxLEQq.png" height="80%" width="80%" alt=/>

3. Content Inspection
Tool Used: Secure Email Gateway, Sandboxing (e.g., FireEye, Palo Alto Networks)
- Action: Inspect the email content for malicious links or attachments. Use sandboxing to safely open and analyze any attachments or links.
 <img src="https://i.imgur.com/Fv3tEJS.png" height="80%" width="80%" alt=/>

 4. Investigate the Scope in SIEM
 Within your SIEM (like Splunk or QRadar), you can take screenshots of the search queries you use to find similar emails, and the results showing any correlated events.
- Tools: SIEM platform showing search queries and results.
<img src="https://i.imgur.com/lijoBqe.png" height="80%" width="80%" alt=/>

5. Analyze the Email Further
 If you perform a deeper analysis using a sandbox or manual inspection, you can capture screenshots of the analysis environment and any findings (like payloads or malicious scripts).
- Tools: Sandbox environment, email analysis tools.
<img src="https://i.imgur.com/JxRgWSC.png" height="80%" width="80%" alt=/>

6. Network and Endpoint Monitoring
Tool Used: SIEM (e.g., Splunk, QRadar), Endpoint Detection and Response (EDR) (e.g., CrowdStrike, Carbon Black)
- Action: Monitor network traffic and endpoints for any signs of compromise or unusual activity related to the email. Look for any attempts to access the link or download attachments.
<img src="https://i.imgur.com/PXR8dVw.png" height="80%" width="80%" alt=/>

7. Incident Response
Tool Used: Incident Response Platform (e.g., IBM Resilient, TheHive)
- Action: If the email is confirmed to be malicious, initiate the incident response process. Isolate affected systems, block the sender’s domain, and update email filters to prevent similar attacks.
<img src="https://i.imgur.com/SH70yAy.png" height="80%" width="80%" alt=/>

8. User Education and Awareness
Tool Used: Security Awareness Training Platforms (e.g., KnowBe4, PhishMe)
- Action: Conduct a training session to educate employees about the characteristics of whaling attacks and how to recognize and report them.
<img src="https://i.imgur.com/I36hpl2.png" height="80%" width="80%" alt=/>

Finally, after everything's under control, we’d document the whole incident—what happened, how we responded, and what we learned. This helps us refine our detection and response processes so we’re even better prepared next time.


Great example of one many things a SOC ANALYST will face.................

  




</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
