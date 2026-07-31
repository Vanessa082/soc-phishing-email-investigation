# Investigation Methodology

## Purpose

This methodology documents how the two email examples were reviewed without inventing evidence that was unavailable.

## Step 1 - Preserve and sanitize evidence

- Save screenshots of the email and authentication results.
- Copy relevant header fields into a text file.
- Remove personal email addresses and unique identifiers before public publication.
- Keep an unchanged private copy only when organizational policy permits.

## Step 2 - Review visible content

Examine:

- sender display name and address;
- subject line;
- greeting and writing style;
- urgency, fear, authority, or curiosity;
- requests for credentials, money, or sensitive information;
- links and attachments;
- claims of prior conversation or forwarding.

## Step 3 - Review technical headers when available

Examine:

- From;
- Return-Path;
- Received chain;
- Message-ID;
- SPF;
- DKIM;
- DMARC;
- timestamps and time zones.

Authentication results help verify domain use, but a pass does not prove that content is safe. A legitimate or compromised account can still send harmful messages.

## Step 4 - Extract indicators

Record only indicators supported by the evidence:

- sender addresses;
- domains;
- URLs;
- IP addresses;
- file names and hashes;
- behavioral indicators such as urgent payment changes.

Do not fabricate missing indicators.

## Step 5 - Compare evidence

Compare the legitimate message with the phishing sample across sender consistency, authentication, language, requested action, links, attachments, and business risk.

## Step 6 - Classify

Use evidence-based language:

- Benign
- Suspicious
- Phishing
- Business email compromise
- Inconclusive

## Step 7 - Recommend response

Recommendations should match the evidence and possible impact. For financial requests, independent verification and multi-person approval are essential.

## Limitations

- The SANS sample does not include a raw email header.
- No live domain-reputation lookup was performed.
- No link, attachment, malware, or mailbox-wide search was available.
- The Gmail email was a controlled training message, not a real attack.
