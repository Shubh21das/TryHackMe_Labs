# Greenholt Phish: Email Analysis (TryHackMe)

## Scenario

A sales executive at **Greenholt PLC** reported a suspicious email that appeared to come from a known customer. The message raised several red flags:

- Generic greeting
- Unexpected request for a money transfer
- Unsolicited attachment
- Tone and style did not match the customer's usual communication

The email was escalated to the SOC for investigation. The goal is to determine whether it is **legitimate** or a **phishing attempt**.

## Objectives

- Analyze the provided email and extract key artifacts
- Investigate the message source to determine its origin and authenticity
- Use analysis tools to assess whether the email is malicious

## Tools Used

- Email client / text editor (to view the raw `.eml` file)
- Email header analyzer
- WHOIS / IP lookup
- VirusTotal (file hash and URL reputation)
- CyberChef (decoding, hashing)

## Findings

The email was found malicious, deteced as ransomeware and trojan.

## Recommended Actions

- Block the sender address and domain at the email gateway
- Block identified malicious IPs and file hashes
- Delete the email from all affected mailboxes
- Notify the reporting employee and confirm no attachment was opened
- Raise user awareness about spotting phishing red flags

## Key Takeaways

- Always check the sender against the Reply-To address
- SPF, DKIM, and DMARC results help verify the sender's authenticity
- Hash suspicious attachments and check them against threat intelligence sources
- Urgent requests for money transfers are a classic phishing signal

## Disclaimer

These notes are for learning and documentation purposes only.
