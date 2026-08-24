# Phishing Email Analysis Lab

## Overview

A beginner-level SOC investigation project focused on identifying and analyzing
a simulated phishing email using basic email analysis, header investigation,
URL analysis, IOC extraction, and threat intelligence.

## Scenario

A user reported an email claiming to be from Microsoft Security. The message
used urgent language and directed the recipient to verify their account through
a suspicious URL.

The investigation was performed from a SOC L1 analyst perspective.

## Investigation Workflow

Email Analysis
→ Header Analysis
→ URL Analysis
→ IOC Extraction
→ Threat Intelligence
→ Investigation
→ Final Verdict

## Tools Used

- VirusTotal
- Email Header Analysis
- Basic IOC Analysis
- MITRE ATT&CK

## Key Findings

- Microsoft brand impersonation
- Lookalike domain: micros0ft-support.com
- SPF authentication failure
- DMARC authentication failure
- No DKIM signature
- Suspicious verification URL
- Urgent social-engineering language

## Threat Intelligence

VirusTotal result:

0/92 security vendors flagged the domain as malicious.

The absence of detections was not treated as proof that the domain was
legitimate. The final assessment was based on multiple correlated indicators.

## Indicators of Compromise

Sender:
security-alert@micros0ft-support.com

Reply-To:
security-verification@micros0ft-support.com

Domain:
micros0ft-support.com

URL:
https://micros0ft-support.com/verify 
 
## MITRE ATT&CK 
 
T1566.002 - Phishing: Spearphishing Link 
 
The simulated phishing email uses a suspicious link to direct the recipient 
toward a potentially malicious verification page. 
 
## Final Verdict 
 
MALICIOUS / PHISHING 
 
Confidence: HIGH 
 
The email was assessed as a phishing attempt based on the combination of 
brand impersonation, lookalike domain, failed email authentication, suspicious 
URL, and social-engineering techniques. 
 
## SOC Response Recommendations 
 
- Quarantine the email 
- Block the identified domain and URL 
- Search for other recipients 
- Determine whether the user clicked the URL 
- Check whether credentials were submitted 
- Reset credentials if compromise is suspected 
- Monitor the affected account 
 
## Skills Demonstrated 
 
- Phishing Email Analysis 
- Email Header Analysis 
- IOC Extraction 
- URL Investigation 
- Threat Intelligence 
- MITRE ATT&CK Mapping 
- SOC L1 Investigation 
- Incident Documentation do i use # or remove it 
