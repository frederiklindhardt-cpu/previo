# Claude Code — Project Rules

## Puppeteer guardrails

Puppeteer is used solely so Claude can inspect and understand the Previo website during development. The following rules apply at all times:

1. **Own domain only** — only navigate to `previo-group.com` or pages explicitly provided by the user. Do not follow external links unprompted.
2. **No PII in screenshots** — once the product is live and handling real candidate data, do not take screenshots of any page that may contain candidate PII.
