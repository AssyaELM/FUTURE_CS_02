# FUTURE_CS_02  Phishing Email Detection & Awareness

Cyber Security Internship · Future Interns · Task 2
Author: Assia EL MOURTADAH

## Overview
Safe, read-only analysis of 3 real phishing email samples: identify indicators,
classify risk (Safe/Suspicious/Phishing), and provide awareness guidelines.
Educational only no links clicked, no attachments opened.

## Samples
| Sample | Pretends to be | Classification |
|--------|----------------|----------------|
| sample-1002 | Microsoft account team | Phishing |
| sample-1714 | Costco (prize scam) | Phishing |
| sample-1878 | Outlook Support (compromised account) | Phishing |

## Tools Used
- cat / sed / grep (read headers, fields, links)
- Google Admin Toolbox — Messageheader (SPF/DKIM/DMARC)
- VirusTotal, urlscan.io (domain/URL reputation)
- base64 decoder (reveal hidden links)
- Kali Linux (isolated VM)

## Analysis Approach
1. Read each email as plain text.
2. Extract headers + key fields (From, Reply-To, Return-Path, IP, Subject).
3. Check SPF/DKIM/DMARC in the header analyser.
4. Defang and scan domains/links without visiting them.
5. Identify indicators, then classify the risk.

## Ethical Statement
All analysis was passive and conducted on public samples for education only.
