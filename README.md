<div align="center">

# ITSTCK | Open Technical Stack & Knowledge Base

[![Site Status](https://img.shields.io/website?url=https%3A%2F%2Fitstck.com&style=for-the-badge&logo=cloudflare&color=0EA5E9)](https://itstck.com)
[![Built with MkDocs Material](https://img.shields.io/badge/Material_for_MkDocs-526CFE?style=for-the-badge&logo=MaterialForMkDocs&logoColor=white)](https://squidfunk.github.io/mkdocs-material/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](.github/CONTRIBUTING.md)

[🌐 Live Website](https://itstck.com/) • [📚 Blog Hub](https://itstck.com/blog/) • [🤝 Contribute](#contributing) • [📬 Contact](https://itstck.com/contact/)

</div>

---

## Overview

**ITSTCK** is an open-source, enterprise-grade knowledge platform and architectural registry. It consolidates production-tested runbooks, security benchmarks, system administration standards, and modern software design patterns into a unified multi-project architecture powered by **MkDocs Material**.

### Specialization Domains

| Knowledge Domain | Technical Scope | Web Path |
| :--- | :--- | :--- |
| **Systems & Infrastructure** | Cloud (AWS, Azure, GCP), DevOps, Linux Kernel, Networking, SRE, Windows & AD | [`/sys/`](https://itstck.com/sys/) |
| **Cybersecurity & GRC** | Blue Team, Incident Response, GRC (ISO 27001, PCI DSS, NIST CSF), IoT Security, Red Team, Zero Trust | [`/cyb/`](https://itstck.com/cyb/) |
| **Software Engineering** | Clean Architecture, DDD, Async Python, Rust, Micro-Frontends, React/Next.js, Flutter | [`/soft/`](https://itstck.com/soft/) |
| **Data & AI Engineering** | Apache Kafka, Data Warehousing, Agentic AI (LangGraph), PEFT/LoRA Fine-tuning, RAG, MLOps | [`/data/`](https://itstck.com/data/) |
| **Tech Blog** | Technical articles, security writeups, and deep dives | [`/blog/`](https://itstck.com/blog/) |

---

## Monorepo Architecture

This repository operates as a monorepo containing multiple isolated **MkDocs** projects under the `projects/` directory. Each sub-project manages its own `mkdocs.yml` configuration and documentation source tree (`docs/`).

```txt
[itstck.com/]
├── .github/                 # GitHub Actions CI/CD workflows
├── projects/
│   ├── sys/                 # Systems & Infrastructure sub-site
│   ├── cyb/                 # Cybersecurity & GRC sub-site
│   ├── soft/                # Software Engineering sub-site
│   ├── data/                # Data Engineering & AI sub-site
│   └── blog/                # Tech Blog sub-site
├── .gitignore               # Secret scanning & build exclusions
├── CONTRIBUTING.md          # Contribution guidelines
├── LICENSE                  # MIT License
└── README.md                # Repository overview
```

---

## Quickstart & Local Development

### Prerequisites

* **Python 3.10+**
* **Git**

### Installation

1. **Clone the repository:**

```bash
   git clone [https://github.com/it-stck/web.git](https://github.com/it-stck/web.git)
   cd web
```

2. **Create and activate a virtual environment:**

```bash
# On Linux/macOS
python3 -m venv .venv
source .venv/bin/activate

# On Windows (PowerShell)
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

3. **Install dependencies:**

```bash
pip install mkdocs-material mkdocs-rss-plugin
```

4. **Serve a project locally:**

Specify the target project configuration file using the '-f' flag:

```bash
# Serve Systems & Infrastructure
mkdocs serve -f projects/sys/mkdocs.yml

# Serve Cybersecurity & GRC
mkdocs serve -f projects/cyb/mkdocs.yml

# Serve Software Engineering
mkdocs serve -f projects/soft/mkdocs.yml

# Serve Data & AI Engineering
mkdocs serve -f projects/data/mkdocs.yml

# Serve Tech Blog
mkdocs serve -f projects/blog/mkdocs.yml
```

5. **Open in browser:**

Navigate to `http://127.0.0.1:8000/` to preview live updates with hot-reloading.

---

## Theme & Customization

The repository uses custom CSS (`assets/css/extra.css`) designed specifically for **ITSTCK**.
It features:

* **Slate Dark Mode** (Default deep slate with cyan/indigo accents).
* **Light Mode Support** (High-contrast light theme).
* **Custom Typography** (`Inter` for UI and `JetBrains Mono` for code blocks).
* **Responsive Layouts** with adaptive CSS variable definitions.

---

## Metadata & SEO Standard

Every `.md` file inside `docs/` must include a YAML frontmatter header conforming to the following template:

```yaml
---
title: ITSTCK | Article Title Here
canonical_url: [https://itstck.com/domain/path/](https://itstck.com/domain/path/)
description: A concise description of the guide or documentation page.
hide:
  - navigation
  - toc
  - feedback
---
```

---

## Contributing

Contributions are welcome! Please read our ['CONTRIBUTING.md'] guide prior to submitting Pull Requests.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/NewGuide`)
3. Commit your Changes (`git commit -m 'Add new Kubernetes runbook'`)
4. Push to the Branch (`git push origin feature/NewGuide`)
5. Open a Pull Request

---

## License

Distributed under the **MIT License**. See ['LICENSE.md'] for more information.

---

**[ITSTCK](https://itstck.com)** - Open Technical Stack & Knowledge Base

Maintained by the ITSTCK Engineering Community.

---