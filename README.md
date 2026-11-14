<div align="center">

# Syed Anas Mohiuddin

### AI Security Researcher · MCP & Agentic Systems
### Founder of [Cognivators](https://www.cognivators.com)

**I find and fix the security bugs in the plumbing that lets AI agents use tools.**

</div>

---

<div align="center">

| | **The record, at a glance** | |
|:---:|:---|:---:|
| 🐞 | CVEs credited to my name (Google · Rapid7 · AWS ×2) | **4** |
| 🛡️ | Published GitHub Security Advisories crediting me | **17** |
| 🔀 | Security fixes merged by the vendors themselves (GitHub, MongoDB, Uber, Composio, DoiT, Timescale…) | **24** |
| 🏛️ | Open-source projects & organizations that publicly credit me by name | **37** |
| 📨 | Coordinated disclosure reports sent across the ecosystem (2026) | **~280** |
| 🏦 | Governments that fixed bugs I reported (France · Norway · Indonesia) | **3** |

*Every number above links to a primary source below. Nothing on this page is self-attested where a vendor record exists.*

</div>

---

## 🐞 CVEs credited to me

| CVE | Vendor | The bug | Severity | Where I'm named |
|---|---|---|:---:|---|
| [**CVE-2026-14540**](https://www.cve.org/CVERecord?id=CVE-2026-14540) | **Google** — [MCP Toolbox for Databases](https://github.com/googleapis/mcp-toolbox) | SSRF via unrestricted HTTP redirection: a crafted path parameter made the server follow redirects to internal/arbitrary endpoints, from inside the network | **8.0 High** (CVSS 4.0) | CVE record (finder) · [Google's fix PR #3448](https://github.com/googleapis/mcp-toolbox/pull/3448) |
| [**CVE-2026-125271**](https://www.cve.org/CVERecord?id=CVE-2026-125271) | **AWS** — [aws-api-mcp-server](https://github.com/awslabs/mcp) | Security policy bypass: hand-rolled kebab-case normalization broke denyList/elicitList matching for **509 operations** — IAM SAML/OIDC federation, MFA, SSH keys — silently, with no signal to the operator | **High** | [AWS bulletin 2026-176](https://aws.amazon.com/security/security-bulletins/2026-176-aws/) (named thanks) · [GHSA-4wq9-grf3-qg2p](https://github.com/awslabs/mcp/security/advisories/GHSA-4wq9-grf3-qg2p) (analyst) |
| [**CVE-2026-116635**](https://www.cve.org/CVERecord?id=CVE-2026-116635) | **AWS** — [aws-serverless-mcp-server](https://github.com/awslabs/mcp) | Path traversal via unvalidated `project_name`: read/write of arbitrary `.json` files outside the deployment-status directory | **Moderate** | [AWS bulletin 2026-164](https://aws.amazon.com/security/security-bulletins/2026-164-aws/) (named thanks) · [GHSA-r6mm-377j-qg8m](https://github.com/awslabs/mcp/security/advisories/GHSA-r6mm-377j-qg8m) (finder) |
| [**CVE-2026-97228**](https://www.cve.org/CVERecord?id=CVE-2026-97228) | **Rapid7** — [Bulk Export MCP](https://github.com/rapid7/rapid7-bulk-export-mcp) | GraphQL query injection in `get_export_status`, reachable through two tools, under the operator's own API scope | **Low** (2.7) | CVE record (finder, "Independent Researcher") |

---

## 🛡️ Published security advisories (17)

Selected highlights — the full list with all 17 is at **[cognivators.com/advisories](https://cognivators.com/advisories)**:

| Advisory | Project | Severity |
|---|---|:---:|
| [GHSA-f8rf-rcrx-h6r9](https://github.com/datalayer/jupyter-mcp-server/security/advisories/GHSA-f8rf-rcrx-h6r9) | Datalayer · Jupyter MCP Server | **Critical** |
| [GHSA-q3gg-rgxh-gh64](https://github.com/CakeRepository/1Password-MCP/security/advisories/GHSA-q3gg-rgxh-gh64) | 1Password-MCP (community) | **High** |
| [GHSA-93f9-v357-x7m7](https://github.com/ark-forge/mcp-eu-ai-act) | ArkForge · EU AI Act MCP | Medium |
| [GHSA-7hwf-488h-59x8](https://github.com/navikt/copilot) | **NAV (Norwegian Labour & Welfare)** · joint credit | Medium |
| [GHSA-pw2j-pj4h-f5vg](https://github.com/INFOKOM-KI/Wazuh-MCP-Server) | Tangerang (Indonesia) · Wazuh MCP | High |
| [GHSA-x8w3-wqcf-6p5c](https://github.com/DollhouseMCP/mcp-server/security/advisories/GHSA-x8w3-wqcf-6p5c) | DollhouseMCP (macOS safety-dialog bypass) | — |
| [GHSA-m623-vm42-63fg](https://github.com/VeriTeknik/pluggedin-app) | VeriTeknik · pluggedin-app | — |
| [GHSA-hpmc-4g74-v53v](https://github.com/guimatheus92/mcp-video-analyzer) | mcp-video-analyzer (SSRF + 3 bypasses) | — |
| [GHSA-wvxg-744g-6pcg](https://github.com/vitali87/code-graph-rag) | code-graph-rag | — |
| [GHSA-mf4q-589h-8gwx](https://github.com/IMRRD/powershell-mcp) | powershell-mcp | — |
| [GHSA-7cc5-q98r-rjwj](https://github.com/warpfreight/warp-agent-mcp) | warpfreight · warp-agent-mcp | — |

---

## 🔀 Fixes I authored, merged by the vendors

These are **my commits/PRs**, written by me and merged into the official codebases:

- **[GitHub](https://github.com/github/github-mcp-server/pull/3056)** — github-mcp-server #3056 (Go): bearer token now attaches only to configured GitHub hosts, not any host a redirect leads to
- **[MongoDB](https://github.com/mongodb-js/mongodb-mcp-server/pull/1501)** — mongodb-mcp-server #1501 (TypeScript): redacts connection-string secrets leaked from malformed preconfigured connections
- **[Salesforce partner](https://github.com/advancedcommunities/salesforce-mcp-server/pull/16)** — salesforce-mcp-server #16 (TypeScript): command-injection escaping before `exec()`

## 🙏 Fixes the vendors wrote, crediting me by name in the record

- **[Uber](https://github.com/uber/ADR/pull/113)** — ADR #113: *"Thank you to Syed Anas Mohiuddin, independent security researcher, for reporting the gap"* (credential values in collected process arguments)
- **[Composio](https://github.com/ComposioHQ/composio/pull/4318)** — #4318 (CLI credential-file permissions)
- **[DoiT](https://github.com/doitintl/doit-mcp-server/pull/247)** — #247 (generated DELETE tools without server-side approval)
- **[Timescale](https://github.com/timescale/mcp-boilerplate-node/pull/50)** — #50 (reflected XSS on the docs page)
- **[Thales](https://github.com/sanyambassi/ciphertrust-manager-mcp-server/commit/6197cbf4)** — CipherTrust Manager MCP (password/JWT on the process command line), fix commit trailer
- **France — [data.gouv.fr](https://github.com/datagouv/datagouv-mcp/pull/126)** — the official open-data platform: *"Reported by Syed Anas Mohiuddin"*
- **[Meeting-BaaS](https://github.com/Meeting-BaaS/meeting-mcp/pull/5)** · **[GDKsoftware](https://github.com/GDKsoftware/Delphi-MCP-Server/pull/51)** · **[alertmanager-mcp](https://github.com/ntk148v/alertmanager-mcp-server/pull/15)** · **[Vocametrix](https://github.com/Vocametrix/vocametrix-mcp/pull/7)** — each merged with a named credit

## 🏛️ Vendor recognition pages naming me

- **[JPMorgan Chase](https://responsibledisclosure.jpmorganchase.com/hc/en-us/articles/360023828114-Recognition-for-Responsible-Disclosures)** — public Recognition for Responsible Disclosures list (SSRF in the docs-search MCP of jpmorgan-payments/ai; fix [PR #19](https://github.com/jpmorgan-payments/ai/pull/19))
- **[Weaviate Security Hall of Fame](https://github.com/weaviate/security-hall-of-fame)** — SSRF in the Google-backed modules; fix [weaviate #12961](https://github.com/weaviate/weaviate/pull/12961)
- **[Amazon Web Services](https://aws.amazon.com/security/security-bulletins/2026-164-aws/)** — security bulletins 2026-164 & 2026-176, coordinated-disclosure acknowledgement

---

<div align="center">

## 🛡️ The tool behind the record: [mcp-safeguard](https://github.com/SyedAnas01/mcp-safeguard)

</div>

**Every CVE above was found with my own scanner.**

```bash
pip install mcp-safeguard
mcp-safeguard scan your-config.json      # or scan-source ./server/
```

An open-source static-analysis security scanner for **MCP servers** — the standard connecting AI agents (Claude, Cursor, GPT) to tools, files, and APIs:

- **148 rules across 7 categories**: prompt injection · credential exposure · SSRF · tool poisoning · endpoint exposure · OAuth scope risk · source audit
- Each finding carries a **severity, a CVSS score, and a fix**; output as text, JSON, HTML, or SARIF for CI
- 252 tests · CI on Python 3.11–3.13 · 9 PyPI releases · **listed in the official MCP registry**
- Runs as a CLI, in CI, or as an MCP server itself
- Listed at [mcp-safeguard.com](https://mcp-safeguard.com) · [PyPI](https://pypi.org/project/mcp-safeguard/) · [official registry](https://registry.modelcontextprotocol.io)

Findings made with it have been **confirmed and fixed by the security teams of Google, GitHub, Rapid7, AWS, JPMorgan Chase, and Weaviate.**

---

## 📄 Research & publications

| Work | Where |
|---|---|
| **Never Emitted: Reporter Attribution in GitHub's Machine-Readable Vulnerability Records** — measured that GitHub's CVE records and OSV exports drop reporter credit in 0/238 and 0/302 cases; the NVD schema has no credits field at all | [arXiv 2609.33099](https://arxiv.org/html/2609.33099) · [Zenodo DOI 10.5281/zenodo.22119724](https://doi.org/10.5281/zenodo.22119724) · [replication dataset, CC0](https://doi.org/10.5281/zenodo.22119153) |
| **Protocol Pivoting: Cross-Protocol Attack Escalation in Agentic AI Systems** — formalized the attack class where an adversary enters via one agent protocol (MCP) and escalates capabilities through another (A2A/ANP) | [Zenodo DOI 10.5281/zenodo.20371152](https://doi.org/10.5281/zenodo.20371152) |
| **Security Considerations for the Model Context Protocol** — recurring vulnerability classes, automated detection, and mitigations for implementers | [IETF Internet-Draft](https://datatracker.ietf.org/doc/draft-mohiuddin-mcp-security-considerations/) (individual submission) |

---

## 🎤 Talks

| | Event | |
|---|---|---|
| 🎤 | **MCPCon North America** (Linux Foundation) — San Jose, Oct 2026 | ✔ spoken |
| 🔥 | **Black Hat Europe 2026 — Arsenal** — London, Dec 2026 *(mcp-safeguard)* | **upcoming** |

## 📰 Press coverage of my research

- **[Ars Technica](https://arstechnica.com/security/2026/10/vulnerability-in-agents-from-google-and-others-exposes-structural-flaw-in-mcp/)** — Dan Goodin: *"MCP may be the riskiest protocol you've never heard of"* (feature on my five-organization SSRF finding + Protocol Pivoting)
- **[The Next Web](https://thenextweb.com/news/mcp-flaw-ssrf-google-jpmorgan-dinum-protocol-pivoting)** — *"Google, JPMorgan and two governments fixed the same MCP flaw"*
- **[Unite.AI](https://www.unite.ai/researcher-discloses-same-mcp-flaw-at-google-jpmorgan-two-governments/)** · **[AI.info](https://ai.info/news/mohiuddin-mcp-security-bugs-five-organizations)** · **[timesof.ai](https://timesof.ai/2026/10/mcp-protocol-pivoting-cross-agent-ssrf)** · **[MCP Store](https://www.mcpstore.nl/en/news/mcp-ssrf-protocol-pivoting/)**

---

<div align="center">

## 💼 Hire me / work with me

</div>

Through **[Cognivators](https://www.cognivators.com)** — AI agent & MCP server security:

- **MCP server security review** — fixed scope, report + retest, priced per engagement
- **AI agent attack-surface assessment** — trust boundaries, tool poisoning, protocol-level risk
- **Security advisory** on shipping agent infrastructure safely

📧 **anas.syed@cognivators.com** · [cognivators.com](https://www.cognivators.com) · [disclosure policy](https://cognivators.com/disclosure) · [PGP key](https://cognivators.com/.well-known/pgp-key.asc)

<div align="center">

---

*Coordinated disclosure only: every finding above was reported privately first, fixed, then published.*

*Previously: data engineering (Apache Spark), ML systems, clinical AI — [older work here](https://github.com/SyedAnas01?tab=repositories).*

</div>