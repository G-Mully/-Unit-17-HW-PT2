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

### Finding 1
Machine IP: 129.168.0.20<br>
Hostname: MSEDGEWIN10<br>
Vulnerability Exploited:<br>
- exploit/windows/http/icecast_header<br>
- Port 8000/tcp open - Icecast streaming media server

<br>


<b>Vulnerability Explanation:</b>
Icecast is an audio broadcast system that streams music in both MP3 and
Ogg Vorbis format. The Icecast server accepts a maximum of 32 headers in the clients HTTP request.

In some environments (like in Win32) a request with more than 31 headers causes the overwriting of the return address of the vulnerable function with a pointer to the beginning of the 32th header.

In short, is possible to execute remote code simply using the normal
HTTP request plus 31 headers followed by a shellcode that will be
executed directly without the need of calling/jumping to registers or
addresses or using other annoying techniques.

<br>

Severity: 
CVSS Score - 7.5 (HIGH)

| Area Impact     | Severity | Outcome                                                                                                                                                                                   |
|-----------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Confidentiality | Partial  | There is considerable informational disclosure                                                                                                                                            |
| Integrity       | Partial  | Modification of some system files or information is possible, but the  attacker does not have control over what can be modified, or the scope  of what the attacker can affect is limited |
| Availability    | Partial  | There is reduced performance or interruptions in resource availability                                                                                                                    |                                        
---


<br>

### Finding 2
Machine IP: 129.168.0.20<br>
Hostname: MSEDGEWIN10<br>

Vulnerability Exploited:<br>
- exploit/windows/local/ikeext_service<br>

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