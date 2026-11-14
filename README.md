<div align="center">

# Syed Anas Mohiuddin

### AI Security Researcher · MCP & Agentic Systems · Founder of [Cognivators](https://www.cognivators.com)

**I find and fix the security bugs in the plumbing that lets AI agents use tools.**

Credited in **4 CVEs** (Google · Rapid7 · AWS ×2) · **17 published security advisories** · named on the security recognition pages of **JPMorgan Chase, Weaviate, and Amazon Web Services** · featured by **Ars Technica** · speaking at **Black Hat Europe 2026**

**📍 Chicago → London (Dec 2026)** · 📧 [anas.syed@cognivators.com](mailto:anas.syed@cognivators.com) · 🔗 [cognivators.com](https://www.cognivators.com) · [advisory list](https://cognivators.com/advisories) · [research](https://www.cognivators.com/founder/research)

**Open to:** security research roles · MCP/agentic-security consulting · contract pentesting

</div>

---

## 🐞 CVEs credited to my name (4, all verifiable)

| CVE | Vendor | The bug | Severity |
|---|---|:---:|---|
| [**CVE-2026-14540**](https://www.cve.org/CVERecord?id=CVE-2026-14540) | **Google** — [MCP Toolbox for Databases](https://github.com/googleapis/mcp-toolbox) | SSRF via unrestricted HTTP redirection — crafted path parameter made the server follow redirects to internal endpoints | **8.0 High** |
| [**CVE-2026-125271**](https://www.cve.org/CVERecord?id=CVE-2026-125271) | **AWS** — [aws-api-mcp-server](https://github.com/awslabs/mcp) | Security policy bypass: broken kebab-case normalization silently defeated the denyList for **509 AWS operations** — IAM federation, MFA, SSH keys | **High** |
| [**CVE-2026-116635**](https://www.cve.org/CVERecord?id=CVE-2026-116635) | **AWS** — [aws-serverless-mcp-server](https://github.com/awslabs/mcp) | Path traversal via unvalidated `project_name` — read/write `.json` outside the deployment-status directory | **Moderate** |
| [**CVE-2026-97228**](https://www.cve.org/CVERecord?id=CVE-2026-97228) | **Rapid7** — [Bulk Export MCP](https://github.com/rapid7/rapid7-bulk-export-mcp) | GraphQL query injection in the export status lookup | Low |

## 🛡️ Published advisories & vendor recognition (17 total)

Selected — **[full list of all 17 →](https://cognivators.com/advisories)**

| Recognition | Where I'm named |
|---|---|
| [**Datalayer · Jupyter MCP Server**](https://github.com/datalayer/jupyter-mcp-server/security/advisories/GHSA-f8rf-rcrx-h6r9) | Critical advisory, credited reporter |
| [**1Password-MCP**](https://github.com/CakeRepository/1Password-MCP/security/advisories/GHSA-q3gg-rgxh-gh64) (community) | High advisory, credited finder |
| [**JPMorgan Chase**](https://responsibledisclosure.jpmorganchase.com/hc/en-us/articles/360023828114-Recognition-for-Responsible-Disclosures) | Public Recognition for Responsible Disclosures list |
| [**Weaviate**](https://github.com/weaviate/security-hall-of-fame) | Security Hall of Fame — SSRF, Aug 2026 |
| [**Amazon Web Services**](https://aws.amazon.com/security/security-bulletins/2026-164-aws/) | Security bulletins 2026-164 & 2026-176 — named thanks |
| [**Uber**](https://github.com/uber/ADR/pull/113) · [**Composio**](https://github.com/ComposioHQ/composio/pull/4318) · [**DoiT**](https://github.com/doitintl/doit-mcp-server/pull/247) · [**Timescale**](https://github.com/timescale/mcp-boilerplate-node/pull/50) | Merged security fixes, credited by name in the PR |
| **NAV Norway** ([GHSA-7hwf-488h-59x8](https://github.com/navikt/copilot), joint) · **France [data.gouv.fr](https://github.com/datagouv/datagouv-mcp/pull/126)** · **Tangerang, Indonesia** ([Wazuh-MCP GHSA](https://github.com/INFOKOM-KI/Wazuh-MCP-Server)) | Government fixes crediting me by name |

## 🔀 Security fixes I authored, merged by the vendors

- **[GitHub's official MCP server](https://github.com/github/github-mcp-server/pull/3056)** #3056 (Go) — bearer token attaches only to configured GitHub hosts
- **[MongoDB's official MCP server](https://github.com/mongodb-js/mongodb-mcp-server/pull/1501)** #1501 (TypeScript) — connection-string secret redaction
- **[salesforce-mcp-server](https://github.com/advancedcommunities/salesforce-mcp-server/pull/16)** #16 — command-injection escaping

---

## 🛡️ The engine: [mcp-safeguard](https://github.com/SyedAnas01/mcp-safeguard) — every CVE above was found with it

```bash
pip install mcp-safeguard && mcp-safeguard scan your-config.json
```

Open-source static-analysis security scanner for **MCP servers** — the standard connecting AI agents (Claude, Cursor, GPT) to tools, files, and APIs. **148 rules, 7 categories** (prompt injection · credential exposure · SSRF · tool poisoning · endpoint exposure · OAuth scope · source audit), each finding with severity, CVSS, and a fix. 252 tests · CI on 3.11–3.13 · **official MCP registry listing** · runs as CLI, in CI, or as an MCP server itself. Findings from it have been confirmed and fixed by **Google, GitHub, Rapid7, AWS, JPMorgan Chase, and Weaviate**.

→ [mcp-safeguard.com](https://mcp-safeguard.com) · [PyPI](https://pypi.org/project/mcp-safeguard/)

---

## 📄 Research & standards

- **Never Emitted** — reporter attribution lost in GitHub's machine-readable CVE/OSV/NVD records (0/238, 0/302, 0/43) → [arXiv 2609.33099](https://arxiv.org/html/2609.33099) · [Zenodo DOI](https://doi.org/10.5281/zenodo.22119724) · [CC0 replication dataset](https://doi.org/10.5281/zenodo.22119153)
- **Protocol Pivoting** — cross-protocol attack escalation in agentic AI (MCP → A2A/ANP) → [Zenodo DOI](https://doi.org/10.5281/zenodo.20371152)
- **IETF Internet-Draft** — Security Considerations for MCP → [datatracker](https://datatracker.ietf.org/doc/draft-mohiuddin-mcp-security-considerations/)

## 🎤 Talks & 📰 press

- 🎤 **MCPCon North America** (Linux Foundation), San Jose — Oct 2026 · 🔥 **Black Hat Europe 2026 Arsenal**, London — Dec 2026 *(upcoming)*
- 📰 [**Ars Technica**](https://arstechnica.com/security/2026/10/vulnerability-in-agents-from-google-and-others-exposes-structural-flaw-in-mcp/) · [**The Next Web**](https://thenextweb.com/news/mcp-flaw-ssrf-google-jpmorgan-dinum-protocol-pivoting) · [**Unite.AI**](https://www.unite.ai/researcher-discloses-same-mcp-flaw-at-google-jpmorgan-two-governments/) · [AI.info](https://ai.info/news/mohiuddin-mcp-security-bugs-five-organizations) · [timesof.ai](https://timesof.ai/2026/10/mcp-protocol-pivoting-cross-agent-ssrf) · [MCP Store](https://www.mcpstore.nl/en/news/mcp-ssrf-protocol-pivoting/)

---

## 💼 Work with me

Through **[Cognivators](https://www.cognivators.com)**:
- **MCP server security review** — fixed scope, report + retest
- **AI agent attack-surface assessment** — trust boundaries, tool poisoning, protocol-level risk
- **Advisory** on shipping agent infrastructure safely

*Coordinated disclosure only — every finding above was reported privately, fixed, then published. Vulnerability in something of mine? [security@cognivators.com](mailto:security@cognivators.com) · [PGP](https://cognivators.com/.well-known/pgp-key.asc) · [disclosure policy](https://cognivators.com/disclosure)*