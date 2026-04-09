# Claude Code — Project Rules

## Project overview

Previo Group — automated pre-employment screening platform targeting regulated and reputation-sensitive hiring across UK/EU (regulated firms, political parties, professional services, senior leadership). This repo contains the landing page, strategy docs, outreach setup, and brand guidelines.

- **Live site:** previo-group.com
- **OpenClaw outreach agent:** running on Mac Mini (`sshuser@100.111.26.59`), see `OPENCLAW-SETUP.md` for full details

## Puppeteer guardrails

Puppeteer is used solely so Claude can inspect and understand the Previo website during development. The following rules apply at all times:

1. **Own domain only** — only navigate to `previo-group.com` or pages explicitly provided by the user. Do not follow external links unprompted.
2. **No PII in screenshots** — once the product is live and handling real candidate data, do not take screenshots of any page that may contain candidate PII.
