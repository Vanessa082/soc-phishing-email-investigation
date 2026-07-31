# SANS Phishing Sample Description

## Source

- **Title:** *Defend Your Business Against Phishing*
- **Author:** Matt Bromiley
- **Publisher:** SANS Institute
- **Published:** January 2019
- **Relevant pages:** 3-4 of the supplied PDF
- **Sample type:** Business email compromise (BEC) / payment-redirection phishing

## Scenario shown in the sample

A message that appears to come from a trusted colleague forwards supposed wiring instructions. The embedded request asks the recipient to change payment details for a business associate and provides a new routing number and account number.

## Visible warning signs identified by SANS

1. **Look-alike domain:** The sample contrasts `acmeabc.com` with `acmeacb.com`. The letters are rearranged to create a domain that may be overlooked.
2. **Risky timing:** The message is sent at 4:55 PM on a Friday, when accounting staff may be rushed or distracted.
3. **Urgency:** The message says the new wiring instructions are needed “today” and that the change must be completed “tonight.”
4. **Fabricated trust context:** The email is formatted to look like a forwarded message from a trusted person.
5. **Financial process change:** It requests a change to routing and account information, which could redirect a legitimate payment.

## Evidence limitation

The source shows the visible email and explains its social-engineering indicators. It does not provide the complete raw `.eml` file or full message headers. Therefore, this project does not claim SPF, DKIM, DMARC, Return-Path, source-IP, or attachment-analysis results for this sample.

## Safe handling

The sample is a static educational image. No active link, attachment, malware, or credential-harvesting page is included in this repository.
