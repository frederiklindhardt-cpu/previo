# Previo Group

**Know who you hire — before you hire them.**

Previo Group is an automated pre-employment screening platform that uses OSINT-based intelligence and compliance-first scoring to give employers full visibility into candidates before making hiring decisions.

---

## What We're Building

A modern screening platform that replaces slow, manual background checks with automated, score-driven candidate intelligence. Think credit score, but for hiring risk.

### Core Capabilities

- **Compliance Score** — A single, auditable risk score per candidate covering sanctions, adverse media, professional identity, and court records
- **Sanctions & Watchlist Screening** — Real-time checks against global sanctions lists, PEP databases, and enforcement registries
- **Adverse Media Monitoring** — OSINT-powered media screening with NLP-based sentiment and relevance filtering
- **Professional Identity Verification** — Cross-referencing claimed qualifications, employment history, and professional registrations
- **Court & Criminal Records** — Jurisdiction-aware record checks with automated data retrieval
- **Audit-Ready Reporting** — Full audit trails, GDPR/DPA 2018 compliant data handling, exportable compliance reports
- **ATS Integrations** — Plug into existing hiring workflows via API and native integrations

### Target Market

UK/EU financial services firms hiring for regulated roles (FCA-regulated, PRA-supervised). This is our wedge — the segment with the highest compliance burden and weakest existing tooling.

---

## Tech Stack (Planned)

| Layer | Tech | Notes |
|-------|------|-------|
| Frontend | Next.js / React | Dashboard, candidate reports, score UI |
| Backend | Node.js or Python (FastAPI) | API layer, scoring engine, integrations |
| Database | PostgreSQL | Candidate data, audit logs, screening results |
| Search/OSINT | Elasticsearch | Media indexing, entity resolution |
| Queue | Redis / BullMQ | Async screening job processing |
| Auth | Auth0 or Clerk | SSO for enterprise clients |
| Infra | AWS or Vercel + AWS | Hosting, storage, compliance (EU region) |
| CI/CD | GitHub Actions | Automated testing, deployment |

> Stack decisions are not final — will be validated during build phase.

---

## Project Structure (Planned)

```
previo-group/
├── apps/
│   ├── web/              # Next.js frontend (dashboard + landing)
│   ├── api/              # Backend API service
│   └── worker/           # Background screening job processor
├── packages/
│   ├── scoring/          # Compliance score calculation engine
│   ├── osint/            # OSINT data retrieval modules
│   ├── integrations/     # ATS connectors (Workday, Greenhouse, etc.)
│   └── shared/           # Shared types, utils, config
├── docs/                 # Architecture docs, API specs, compliance notes
├── .github/
│   └── workflows/        # CI/CD pipelines
├── docker-compose.yml
├── package.json          # Monorepo root (pnpm workspaces or turborepo)
└── README.md
```

---

## Regulatory & Compliance Context

This product operates in a heavily regulated space. Key frameworks:

- **GDPR** (EU General Data Protection Regulation)
- **UK DPA 2018** (Data Protection Act)
- **FCA/PRA** requirements for regulated role screening
- **ISO 27001** (target certification for enterprise sales)
- **FCRA** (if/when expanding to US market)

Data residency, consent management, right to erasure, and lawful basis for processing are first-class concerns — not afterthoughts.

---

## Go-To-Market Strategy

**Phase 1 — Validate (current)**
- Landing page live at [previo-group.com](https://previo-group.com)
- Email waitlist for early interest
- Market analysis completed (competitor landscape, white space mapping)

**Phase 2 — Build MVP**
- Core screening flow: candidate in → score out
- Single integration (likely Greenhouse or Workable)
- Manual + automated hybrid for initial checks

**Phase 3 — Scale**
- Full automation across all screening pillars
- Multi-ATS integration
- Self-serve onboarding for SMB tier
- Enterprise sales motion for regulated firms

---

## Competitive Landscape

Key incumbents: First Advantage, Sterling, HireRight, Checkr, Veremark, Certn, Intelligo.

Our differentiation:
1. **Score-first UX** — single compliance score vs. walls of PDF reports
2. **OSINT-native** — built on open source intelligence from day one, not just database lookups
3. **UK/EU compliance-first** — GDPR and DPA 2018 baked in, not bolted on
4. **Speed** — automated pipeline vs. 3-5 day manual turnaround

---

## Development

```bash
# Clone the repo
git clone https://github.com/YOUR_ORG/previo-group.git
cd previo-group

# Install dependencies (once project is scaffolded)
pnpm install

# Run development environment
pnpm dev
```

---

## Links

- **Website:** [previo-group.com](https://previo-group.com)
- **Contact:** hello@previo-group.com

---

## License

Proprietary. All rights reserved.
