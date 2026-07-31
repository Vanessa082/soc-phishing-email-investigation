# SANS Phishing Sample - Analysis Notes

## Initial triage

- **Sample category:** Business email compromise (BEC)
- **Targeted business function:** Accounting / accounts payable
- **Requested action:** Change payment wiring instructions
- **Potential impact:** Unauthorized transfer of company funds
- **Recommended severity:** High in a real organization

## Evidence observations

| Evidence | Observation | Why it matters |
|---|---|---|
| Sender domain | `acmeacb.com` | Closely resembles `acmeabc.com`; likely intended to evade quick visual review. |
| Message timing | Friday at 4:55 PM | The recipient may be rushed near close of business and month-end activities. |
| Urgency | “today,” “immediately,” and “tonight” | Pressure can discourage independent verification. |
| Financial request | Change routing and account details | A successful response could redirect a legitimate payment. |
| Forwarded-message appearance | Embedded message appears to come from another trusted employee | Creates false familiarity and authority. |
| Verification path | No independent confirmation is shown | High-risk payment changes should be verified outside the email thread. |

## IOC discussion

Traditional IOCs often include IP addresses, URLs, file hashes, domains, and sender addresses. This sample supplies only a visible look-alike domain. The strongest evidence is therefore a combination of:

- the look-alike domain;
- the urgent payment-change request;
- suspicious timing;
- and the fabricated forwarded-message context.

The routing number and account number are displayed as fictional content in a training document and are not treated as active malicious infrastructure.

## Analyst assessment

The sample is consistent with business email compromise phishing. It attempts to impersonate trusted employees and redirect a business payment using a look-alike domain, urgency, and a fake forwarded conversation.

## Recommended actions

1. Do not modify payment instructions based solely on the email.
2. Contact the supposed sender using a previously known phone number or another trusted channel.
3. Notify the security and finance teams.
4. Search the mail environment for messages using the look-alike domain.
5. Block the look-alike domain when organizational controls and investigation findings justify it.
6. Review whether any employee acted on the request.
7. Require multi-person approval for payment-detail changes.
