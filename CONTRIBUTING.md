# Contributing to ITSTCK

Thank you for taking the time to contribute to **ITSTCK**! We welcome community contributions, improvements, corrections, and new enterprise technical guides.

---

## Code of Conduct

* Keep all technical discussions respectful, professional, and constructive.
* Focus on providing high-quality, verified, and production-ready information.
* Avoid marketing pitches, unsolicited self-promotion, or low-effort AI-generated spam.

---

## How to Contribute

### 1. Reporting Issues or Content Fixes

* If you discover a broken command, outdated configuration, security gap, or typo, please open a **GitHub Issue**.
* Be specific about the file path (e.g., `projects/sys/docs/cloud/guides/aws-threat-detection.md`) and provide details on how to reproduce or fix the issue.

### 2. Submitting New Content or Improvements

1. **Fork the Repository:** Create your personal fork of [`it-stck/web`](https://github.com/it-stck/web).

2. **Create a Feature Branch:**

```bash
   git checkout -b docs/add-kubernetes-hardening-guide
```

3. **Add or Modify Content:** Make your changes within the appropriate project folder under `projects/`.

---

## Frontmatter & Metadata Rules

Every Markdown file (`.md`) submitted to the repository **must** include the following frontmatter header at the top of the file:

```yaml
---
title: ITSTCK | Your Article or Guide Title
canonical_url: [https://itstck.com/path/to/page/](https://itstck.com/path/to/page/)
description: A concise 1-2 sentence description of the content for SEO and preview cards.
hide:
  - navigation
  - toc
  - feedback
---
```

---

## Local Testing Workflow

Before opening a Pull Request, verify that your changes render properly without errors or broken links:

1. **Set up virtual environment:**

```bash
python -m venv .venv
source .venv/bin/activate  # On Windows: .\.venv\Scripts\Activate.ps1
pip install mkdocs-material mkdocs-rss-plugin
```

2. **Serve the target project locally:**

```bash
# Example for Systems & Infrastructure
mkdocs serve -f projects/sys/mkdocs.yml
```

3. **Verify rendering:** Check `http://127.0.0.1:8000/` in your browser to confirm there are no layout or syntax issues.

---

## Security & Secret Scanning

* **DO NOT commit real credentials, API keys, tokens, or private IP addresses.**
* Always sanitize examples using generic placeholders (e.g., `example.com`, `YOUR_API_KEY`, `192.168.1.X`).
* The repository enforces GitHub Push Protection; commits containing active secrets will be automatically rejected.

---

## Submitting a Pull Request

1. Commit your changes with a clear, concise commit message:

```bash
git commit -m "docs(sys): add AWS GuardDuty configuration runbook"
```

2. Push to your fork:

```bash
git push origin docs/add-kubernetes-hardening-guide
```

3. Open a **Pull Request** against the `main` branch of `it-stck/web`. Provide a brief summary of what was added or updated.

---
