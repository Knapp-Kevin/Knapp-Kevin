<div align="center">

<img src="https://avatars.githubusercontent.com/u/205245245?v=4" width="145" alt="Kevin Knapp">

# Kevin Knapp

**Lead AI Product Engineer · Agent Governance Architect · Open-Source Standards Contributor**

[Bicameral](https://www.linkedin.com/company/bicameral-ai/) · [MythologIQ Labs](https://www.linkedin.com/company/mythologiq/) · [Microsoft Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit) · [AgenTrust Agent Manifest](https://github.com/agentrust-io/agent-manifest)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Kevin%20Knapp-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kevin-r-knapp/)
[![Public work](https://img.shields.io/badge/Public%20Work-Curated%20Index-2563eb?style=flat-square&logo=github&logoColor=white)](PUBLIC_WORK.md)

</div>

> **Governance by prompt is not real governance.** Reliable agent governance requires deterministic enforcement, explicit authority boundaries, verifiable provenance, and evidence that survives outside the model's own reasoning.

## What I build

I work on trustworthy autonomous-agent systems: policy enforcement, authority and identity boundaries, persistent state, evidence provenance, MCP-mediated workflows, governed ingestion, adversarial validation, and machine-verifiable release controls.

My work spans three complementary layers:

- **Open standards and shared infrastructure:** AgenTrust Agent Manifest and Microsoft's Agent Governance Toolkit.
- **Production agent systems:** Bicameral, where I work across governed local-first agent runtime, MCP, evidence ingestion, authority boundaries, deterministic validation, and release evidence.
- **Independent R&D:** MythologIQ Labs, where I build governance, safety, local inference, privacy, and agent-development tooling.

## Selected contributions

These links are intentionally specific. They show the work, review history, and implementation context rather than asking a profile paragraph to do all the convincing.

| Area | Contribution | Evidence |
| --- | --- | --- |
| **AgenTrust · Agent Manifest** | Designed the v0.2 incremental memory checkpoint/delta binding protocol for governed persistent agent memory, using RFC 9162 consistency proofs and fail-closed drift semantics. | [Issue #174](https://github.com/agentrust-io/agent-manifest/issues/174) · [PR #190](https://github.com/agentrust-io/agent-manifest/pull/190) |
| **Microsoft AGT** | Governed accumulated context across delegated multi-agent workflows. | [PR #2800](https://github.com/microsoft/agent-governance-toolkit/pull/2800) |
| **Microsoft AGT** | Hardened contributor-reputation heuristics for organizational and domain-specialist contributors. | [PR #2852](https://github.com/microsoft/agent-governance-toolkit/pull/2852) |
| **Microsoft AGT** | MCP trust-verification integration guidance and reference implementation. | [PR #747](https://github.com/microsoft/agent-governance-toolkit/pull/747) |
| **Bicameral** | Built a provider-neutral ingestion path with GitHub reference acquisition, security screening, evidence identity, and lifecycle tracing. | [Integrations PR #255](https://github.com/BicameralAI/bicameral-integrations/pull/255) |
| **Bicameral** | Implemented governed real-data conformance and redaction evidence with tamper-evident transformation lineage and fail-closed handling. | [Integrations PR #269](https://github.com/BicameralAI/bicameral-integrations/pull/269) |
| **Bicameral** | Added deterministic validation and decision-evidence gates for adversarial redaction-backend evaluation. | [Integrations PR #287](https://github.com/BicameralAI/bicameral-integrations/pull/287) |

[**View the broader public-work index →**](PUBLIC_WORK.md)

## Engineering focus

<table>
<tr>
<td width="50%" valign="top">

### Governance and authority

- Deterministic policy enforcement
- Fail-closed security boundaries
- Capability and authority mediation
- Human approval and confirmation contracts
- Spec-to-runtime conformance
- Agent and contributor trust models

</td>
<td width="50%" valign="top">

### Evidence and state

- Provenance and transformation lineage
- Tamper-evident audit structures
- Persistent agent memory governance
- Replay, currentness, and idempotency
- Adversarial and negative-path testing
- Evidence-bound release controls

</td>
</tr>
</table>

## Selected systems

| Project | Role / relevance |
| --- | --- |
| **[Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit)** | Maintainer / contributor to open governance infrastructure for autonomous agents. |
| **[Agent Manifest](https://github.com/agentrust-io/agent-manifest)** | Contributor to verifiable agent identity/state specification and SDK behavior. |
| **[Bicameral Integrations](https://github.com/BicameralAI/bicameral-integrations)** | Publicly inspectable portion of my Bicameral work: acquisition, normalization, redaction, provenance, evidence, and governed evaluation. |
| **[FailSafe](https://github.com/MythologIQ-Labs-LLC/FailSafe)** | MythologIQ deterministic governance layer for accountable agent execution. |
| **[Qor-Logic](https://github.com/MythologIQ-Labs-LLC/Qor-logic)** | Governance framework for agent-driven software development and evidence-bound workflows. |
| **[presidio-rs](https://github.com/MythologIQ-Labs-LLC/presidio-rs)** | Rust-oriented privacy and redaction infrastructure. |
| **[GG-CORE](https://github.com/MythologIQ-Labs-LLC/GG-CORE)** | Local inference runtime and integration surface. |

> Some production Bicameral and MythologIQ repositories are private. I describe that work where relevant, but use public repositories and PRs above as the independently inspectable evidence surface.

## Operating principles

1. **Deny by default.** Authority is earned for the action being attempted, not inherited from a vague session-level trust state.
2. **Provenance over phrasing.** Where an instruction, artifact, or decision came from matters more than how confidently it is worded.
3. **Stable identity over presentation.** IDs, digests, specifications, and exact state bind authority. Display order and prose do not.
4. **Negative paths are part of the contract.** A system is not governed if stale state, replay, partial failure, or unauthorized mutation are undefined.
5. **Evidence should outlive the agent.** Important decisions need inspectable artifacts, not a claim that the model considered them.

## Toolset

**Languages:** Python · Rust · TypeScript · Go  
**Agent systems:** MCP · agent orchestration · local inference · RAG · governed memory  
**Security / trust:** Ed25519 · policy engines · capability mediation · provenance · redaction · tamper-evident ledgers  
**Platform:** GitHub Actions · Docker · PostgreSQL · SQLite · FastAPI · Tauri

<div align="center">

### Activity

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Knapp-Kevin&custom_title=Contribution%20Activity&bg_color=0d1117&title_color=3B82F6&color=c9d1d9&line=3B82F6&point=ffffff&area=true&area_color=1e3a8a&hide_border=true" width="100%" alt="Kevin Knapp contribution activity">

</div>

---

<div align="center">

**MythologIQ Labs, LLC** · governed agents · verifiable trails · accountable autonomy

[LinkedIn](https://www.linkedin.com/in/kevin-r-knapp/) · [MythologIQ Labs](https://www.linkedin.com/company/mythologiq/) · [Bicameral](https://www.linkedin.com/company/bicameral-ai/) · [Public Work](PUBLIC_WORK.md)

</div>
