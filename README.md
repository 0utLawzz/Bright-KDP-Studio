# KDP Studio

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?logo=typescript&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![pnpm](https://img.shields.io/badge/pnpm-workspaces-F69220)
![Status](https://img.shields.io/badge/Status-Active-success)

> Publishing workspace for planning, validating, generating, and organizing differentiated **Bright Mindful Pages** KDP planners, journals, and trackers.

Prepares print-ready interiors, full-wrap covers, and listing metadata for Amazon KDP. Does **not** scrape Amazon or automate unofficial uploads.

---

## Features

| Area | Capability |
|------|------------|
| Projects | Organize book projects, templates, palettes, tasks |
| Validation | KDP page-count and margin rules before generation |
| Generation | Print-ready interior + full-wrap cover PDFs (ReportLab) |
| Metadata | KDP listing fields and editable template packages |
| Status | Track planned → generated → manually published |

---

## KDP guardrails

- 0.4 in safe margin on every interior page  
- 72-page minimum for color interiors  
- Spine text only at 79+ pages  
- No copyrighted or scraped content  
- No near-identical color-only variants  

---

## Tech stack

| Layer | Choice |
|-------|--------|
| Monorepo | pnpm workspaces |
| UI | React + Vite (`artifacts/kdp-studio`) |
| API | Express + Python/ReportLab generators |
| DB | PostgreSQL + Drizzle |
| Contracts | OpenAPI (`lib/api-spec`) |

---

## Install & run

### Prerequisites

- Node.js 20+
- **pnpm** (required)
- Python 3 (for ReportLab — installed via postinstall)
- PostgreSQL (`DATABASE_URL`)

```bash
git clone https://github.com/0utLawzz/KDP-Studio.git
cd KDP-Studio
pnpm install

# API
pnpm --filter @workspace/api-server run dev

# Web app
pnpm --filter @workspace/kdp-studio run dev
```

Do not commit `.env` or credentials.

---

## Project layout

```text
artifacts/kdp-studio/   React/Vite web app
artifacts/api-server/   Express API + Python/reportlab generators
lib/db/                 Drizzle schema
lib/api-spec/           OpenAPI contract
docs/                   Product specification
```

---

## Contributing & Security

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [SECURITY.md](SECURITY.md)
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)

---

## License

MIT — see [LICENSE](LICENSE).

---

## Author

**Nadeem (OutLawZ)**  
Custom Automation Specialist  

- GitHub: [0utLawzz](https://github.com/0utLawzz)  
- Contact: net2outlawzz@gmail.com  

*Need custom KDP / publishing automation? Contact me.*
