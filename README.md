## GoodSecurity Penetration Test Report

Date: 4/23/2022  
UoT Cybersecurity Bootcamp 2022<br>
G-Mully
([g-mully@GoodSecurity.com](mailto:g-mully@GoodSecurity.com))


<br>

### High-Level Summary
---
GoodSecurity was tasked with performing an internal penetration test on GoodCorps CEO, Hans Gruber. An internal penetration test is a dedicated attack against internally connected systems. The focus of this test is to perform attacks, similar to those of a hacker and attempt to infiltrate Hans computer and determine if it is at risk. GoodSecurity's overall objective was to exploit any vulnerable software and find the secret recipe file on Hans' computer, while reporting the findings back to GoodCorp.

When performing the internal penetration test, there were several alarming vulnerabilities that were identified on Hans' desktop. When performing the attacks, GoodSecurity was able to gain access to his machine and find the secret recipe file by exploiting two programs that had major vulnerabilities. The details of the attack can be found in the Findings category.

---

<br>

### Finding 1
Machine IP: 129.168.0.20<br>
Hostname: MSEDGEWIN10<br>
Vulnerability Exploited:<br>
- exploit/windows/http/icecast_header<br>
- Port 8000/tcp open - Icecast streaming media server

<br>


<b>Vulnerability Explanation:</b>
Icecast application running on 192.168.0.20 allows for a buffer overflow exploit where an attacker can remotely connect and take control of the victim's system by overwriting the memory on the system on utilizing the Icecast flaw, which writes past the end of a pointer array when receiving 32 HTTP headers.

<br>

Severity: 
CVSS Score - 7.5 (HIGH)

| Area Impact     | Severity | Outcome                                                                                                                                                                                   |
|-----------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Confidentiality | Partial  | There is considerable informational disclosure                                                                                                                                            |
| Integrity       | Partial  | Modification of some system files or information is possible, but the  attacker does not have control over what can be modified, or the scope  of what the attacker can affect is limited |
| Availability    | Partial  | There is reduced performance or interruptions in resource availability                                                                                                                    |                                                          

Finding 2
Machine IP:
129.168.0.20
Hostname:
MSEDGEWIN10
Vulnerability Exploited:
exploit/windows/local/ikeext_service
Vulnerability Explanation:
Explain the vulnerability as best you can by explaining the attack type (i.e. is it a heap overflow attack, buffer overflow, file inclusion, etc.?) and briefly summarize what that attack is (Might need Google's help!)
Severity:
In your expert opinion, how severe is this vulnerability?
Proof of Concept:

Finding 3
Machine IP:
129.168.0.20
Hostname:
MSEDGEWIN10
Vulnerability Exploited:
exploit/windows/local/ms16_075_reflection
Vulnerability Explanation:
Explain the vulnerability as best you can by explaining the attack type (i.e. is it a heap overflow attack, buffer overflow, file inclusion, etc.?) and briefly summarize what that attack is (Might need Google's help!)
Severity:
In your expert opinion, how severe is this vulnerability?
Proof of Concept: