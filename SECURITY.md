# Security Policy

## Scope

This repository supports the NK Bag House website project. Security concerns may include exposed credentials, unsafe form handling, access-control issues, vulnerable dependencies, unintended disclosure of enquiry data, or unsafe file uploads.

## Reporting a vulnerability

Please do not publish exploitable vulnerability details, credentials, customer information, or proof-of-concept payloads in a public issue.

If GitHub private vulnerability reporting is enabled for this repository, use the repository's **Security** tab to submit a private report. If it is not enabled, contact the repository owner through a verified private contact channel before sharing sensitive details. Do not send secrets or customer data in a public discussion.

When reporting, include:
- A concise description of the affected area.
- The impact you believe is possible.
- Reproduction steps that do not expose real customer data.
- Relevant versions, commit references, or environment details.
- A safe way to contact you for follow-up, if you want a response.

## Handling reports

The maintainer should acknowledge reports, assess impact, coordinate a fix, and avoid publishing sensitive details before a mitigation is available. Do not promise a response time until a maintainer process has been agreed.

## Development safeguards

- Never commit API keys, passwords, tokens, private keys, or production environment files.
- Keep secrets in environment variables managed by the deployment platform.
- Validate all customer input on the server.
- Apply rate limiting and spam protection to public enquiry endpoints before production.
- Restrict administrative routes and stored enquiry data to authorised users.
- Review third-party dependency updates and licence obligations.
- Avoid logging full enquiry payloads or uploaded file contents.
