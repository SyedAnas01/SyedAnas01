<div align="center">

<!-- Because the shields.io badge API needs a dark-on-light theme to look right on GitHub's light/dark modes -->
<img width="100%" alt="" src="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg'%3E%3C/svg%3E">

# Syed Anas Mohiuddin

### AI Security Researcher · MCP & Agentic Systems

**I find and fix the security bugs in the plumbing that lets AI agents use tools.**

Credited in **4 CVEs** across Google, Rapid7, and AWS · **17 published security advisories** · named on the security recognition pages of **JPMorgan Chase, Weaviate, and Amazon**

[![CVEs](https://img.shields.io/badge/CVEs-4-critical?style=for-the-badge&label=%F0%9F%90%9E%20CVEs%20credited&labelColor=dc2626)](https://www.cve.org/CVERecord?id=CVE-2026-14540)
[![GHSAs](https://img.shields.io/badge/GHSAs-17-important?style=for-the-badge&label=%F0%9F%9B%A1%EF%B8%8F%20Advisories&labelColor=ea580c)](https://cognivators.com/advisories)
[![PyPI](https://img.shields.io/pypi/dm/mcp-safeguard?style=for-the-badge&label=mcp--safeguard&labelColor=0366d6)](https://pypi.org/project/mcp-safeguard/)

<b>cognivators.com</b> · [research & publications ↗](https://www.cognivators.com/founder/research) · [advisory list ↗](https://cognivators.com/advisories) · anas.syed@cognivators.com

</div>

---

## 🐞 CVEs credited to me (all verifiable)

| CVE | Vendor | Bug | Severity |
|---|---|---|---|
| [CVE-2026-14540](https://www.cve.org/CVERecord?id=CVE-2026-14540) | **Google** | SSRF via unrestricted HTTP redirection in MCP Toolbox for Databases | **8.0 High** |
| [CVE-2026-125271](https://www.cve.org/CVERecord?id=CVE-2026-125271) | **AWS** | Security policy bypass via broken operation-name normalization in aws-api-mcp-server — 509 operations silently unmatched | **High** |
| [CVE-2026-116635](https://www.cve.org/CVERecord?id=CVE-2026-116635) | **AWS** | Path traversal in aws-serverless-mcp-server deployment status | Moderate |
| [CVE-2026-97228](https://www.cve.org/CVERecord?id=CVE-2026-97228) | **Rapid7** | GraphQL query injection in Bulk Export MCP | Low |

**Named in vendor recognition pages:** [JPMorgan Chase](https://responsibledisclosure.jpmorganchase.com/hc/en-us/articles/360023828114-Recognition-for-Responsible-Disclosures) (public recognition list) · [Weaviate Security Hall of Fame](https://github.com/weaviate/security-hall-of-fame) (SSRF, Aug 2026) · [AWS security bulletins 2026-164 & 2026-176](https://aws.amazon.com/security/security-bulletins/2026-164-aws/) (coordinated disclosure thanks) · [Uber](https://github.com/uber/ADR/pull/113) (PR credit) · [Composio](https://github.com/ComposioHQ/composio/pull/4318), [DoiT](https://github.com/doitintl/doit-mcp-server/pull/247), [Timescale](https://github.com/timescale/mcp-boilerplate-node/pull/50) (merged security fixes)

**Security fixes I authored, merged by the vendors:** [GitHub's official MCP server #3056](https://github.com/github/github-mcp-server/pull/3056) (Go — bearer-token host allowlisting) · [MongoDB's official MCP server #1501](https://github.com/mongodb-js/mongodb-mcp-server/pull/1501) (TypeScript — connection-string secret redaction) · [salesforce-mcp-server #16](https://github.com/advancedcommunities/salesforce-mcp-server/pull/16) (command-injection escaping)

**Government fixes:** France — [datagouv-mcp #126](https://github.com/datagouv/datagouv-mcp/pull/126) · Indonesia (Tangerang) — GHSA-pw2j-pj4h-f5vg · Norway — NAV (GHSA-7hwf-488h-59x8, joint credit)

---

## 🛡️ mcp-safeguard — the scanner that found them

<div align="center">

[![mcp-safeguard](https://img.shields.io/badge/mcp--safeguard-148%20rules%20·%207%20categories-0366d6?style=flat-square)](https://github.com/SyedAnas01/mcp-safeguard)
[![PyPI](https://img.shields.io/pypi/v/mcp-safeguard?style=flat-square&label=latest%20release)](https://pypi.org/project/mcp-safeguard/)
[![Tests](https://img.shields.io/badge/tests-252%20passing-brightgreen?style=flat-square)](https://github.com/SyedAnas01/mcp-safeguard)
[![License](https://img.shields.io/badge/license-MIT-black?style=flat-square)](https://github.com/SyedAnas01/mcp-safeguard)

</div>

An open-source static-analysis security scanner for **MCP servers** — the standard connecting AI agents (Claude, Cursor, GPT) to tools, files, and APIs. It flags **prompt injection**, **credential exposure**, **SSRF**, **tool poisoning**, **exposed endpoints**, and **OAuth scope risk** in a server's config, tool definitions, and source tree — 148 rules across 7 categories, each finding with severity, CVSS, and a fix. Runs as a CLI, in CI, or as an MCP server itself.

Every CVE above was found with it. **Findings made with this tool have been confirmed and fixed by security teams at Google, GitHub, Rapid7, AWS, JPMorgan Chase, and Weaviate.**

```bash
pip install mcp-safeguard
mcp-safeguard scan your-config.json
```

→ [github.com/SyedAnas01/mcp-safeguard](https://github.com/SyedAnas01/mcp-safeguard) · [mcp-safeguard.com](https://mcp-safeguard.com) · listed in the [official MCP registry](https://registry.modelcontextprotocol.io)

---

## 📄 Research & publications

- **Never Emitted: Reporter Attribution in GitHub's Machine-Readable Vulnerability Records** — [Zenodo DOI 10.5281/zenodo.22119724](https://doi.org/10.5281/zenodo.22119724) · [arXiv 2609.33099](https://arxiv.org/html/2609.33099) — measured that GitHub's CVE records and OSV exports drop reporter credit in 0/238 and 0/302 cases; [replication dataset](https://doi.org/10.5281/zenodo.22119153) (CC0)
- **Protocol Pivoting: Cross-Protocol Attack Escalation in Agentic AI Systems** — [Zenodo DOI 10.5281/zenodo.20371152](https://doi.org/10.5281/zenodo.20371152) — formalized the attack class where an adversary enters through one agent protocol (MCP) and escalates through another (A2A/ANP)
- **IETF Internet-Draft: Security Considerations for MCP Implementations in AI Agent Systems** — [draft-mohiuddin-mcp-security-considerations](https://datatracker.ietf.org/doc/draft-mohiuddin-mcp-security-considerations/) · individual submission

---

## 🎤 Talks & press

- **Speaker**, MCPCon North America (Linux Foundation), San Jose — Oct 2026
- **Accepted**, Black Hat Europe 2026 Arsenal, London — Dec 2026 (mcp-safeguard)
- **Featured**: [Ars Technica](https://arstechnica.com/security/2026/10/vulnerability-in-agents-from-google-and-others-exposes-structural-flaw-in-mcp/) (Dan Goodin) · [The Next Web](https://thenextweb.com/news/mcp-flaw-ssrf-google-jpmorgan-dinum-protocol-pivoting) · [Unite.AI](https://www.unite.ai/researcher-discloses-same-mcp-flaw-at-google-jpmorgan-two-governments/) · AI.info

---

## 📬 Work with me

Through **[Cognivators](https://www.cognivators.com)** — AI agent & MCP security:

- **MCP server security review** — fixed scope, report + retest
- **AI agent attack-surface assessment** — trust boundaries, tool poisoning, protocol-level risks
- **Advisory/consulting** on shipping agent infrastructure safely

Report a vulnerability in anything of mine: `security@cognivators.com` ([PGP](https://cognivators.com/.well-known/pgp-key.asc)) · or find me across the ecosystem on [cognivators.com/research](https://cognivators.com/research)

<div align="center">

**—— 🛡️ ——**

*Coordinated disclosure only. Every finding above was reported privately first, fixed, then published.*

</div>