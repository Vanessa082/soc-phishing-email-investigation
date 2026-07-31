# Phishing Investigation Report

## 1. Executive summary

This investigation compared a real Gmail training message with a public SANS business email compromise sample. The Gmail message passed SPF, DKIM, and DMARC, contained no links or attachments, and clearly identified itself as training. It was classified as benign.

The SANS sample requested an urgent change to business wiring instructions, used a look-alike domain, arrived at a high-pressure time, and created a fake forwarded-message context. It was classified as a phishing/BEC training example.

## 2. Case details

| Field | Value |
|---|---|
| Case ID | SOC-2026-0001 |
| Analyst | Wah Vanessa |
| Date completed | 31 July 2026 |
| Status | Closed |
| Investigation type | Comparative email analysis |
| Data sensitivity | Sanitized training evidence |

## 3. Evidence reviewed

### Legitimate training message

- Gmail inbox screenshot
- Gmail “Show original” authentication summary
- Sanitized message headers
- Message body

### SANS phishing sample

- Sample phishing request shown on page 3 of the supplied SANS paper
- SANS explanation of the warning signs on page 4
- Analyst-created indicator table based only on visible source evidence

## 4. Legitimate email findings

- Sender and Return-Path were consistent.
- The message traveled through Google mail infrastructure.
- SPF passed.
- DKIM passed.
- DMARC passed.
- No links were present.
- No attachments were present.
- No credential or financial request was made.
- The body explicitly described the email as a training exercise.

### Classification

**Benign training email**

Gmail's Spam placement was not treated as proof of maliciousness.

## 5. Phishing sample findings

- The sender used the look-alike domain `acmeacb.com`, resembling `acmeabc.com`.
- The message was sent at 4:55 PM on a Friday.
- It requested new wiring instructions “today” and completion “tonight.”
- It attempted to change routing and account details.
- It appeared to contain a trusted forwarded conversation, but the source explains that this context was fabricated.

### Classification

**Business email compromise phishing sample**

### Potential impact

If successful in a real organization, the request could redirect a legitimate vendor or associate payment to an attacker-controlled account.

## 6. Authentication limitations

The SANS sample did not include complete raw headers. No SPF, DKIM, DMARC, source-IP, Return-Path, or Message-ID conclusion was made for it.

## 7. Recommended response

1. Do not process the payment change.
2. Verify the request through a separate trusted channel.
3. Escalate to security and finance.
4. Search for similar emails and the look-alike domain.
5. Determine whether anyone replied or changed payment details.
6. Consider blocking the look-alike domain.
7. Require multi-person verification for payment-detail changes.
8. Continue phishing-awareness training.

## 8. Final conclusion

The comparison demonstrates that SOC analysis requires both technical evidence and contextual judgment. Email authentication can confirm whether a domain was used consistently, while visible content and business context reveal social-engineering risk. Analysts should document what the evidence supports and clearly state when evidence is missing.
