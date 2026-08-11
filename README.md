<div align="center">

<img src="https://avatars.githubusercontent.com/u/205245245?v=4" width="145" alt="Kevin Knapp">

# Kevin Knapp

**Lead AI Product Engineer · Agent Governance Architect · Open-Source Standards Contributor**

[Bicameral](https://www.linkedin.com/company/bicameral-ai/) · [MythologIQ Labs](https://www.linkedin.com/company/mythologiq/) · [Microsoft Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit) · [AgenTrust](https://github.com/agentrust-io)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Kevin%20Knapp-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kevin-r-knapp/)
[![Technical work](https://img.shields.io/badge/Technical%20Work-Curated%20Index-2563eb?style=flat-square&logo=github&logoColor=white)](PUBLIC_WORK.md)

</div>

> **Governance by prompt is not real governance.** Reliable agent governance requires deterministic enforcement, explicit authority boundaries, verifiable provenance, and evidence that survives outside the model's own reasoning.

## What I build

I work on trustworthy autonomous-agent systems: policy enforcement, authority and identity boundaries, persistent state, evidence provenance, MCP-mediated workflows, governed memory, adversarial validation, and machine-verifiable release controls.

My work spans four complementary layers:

- **Open standards and shared infrastructure:** AgenTrust Agent Manifest and Microsoft's Agent Governance Toolkit.
- **Governed memory architecture:** [Agent Memory](https://github.com/MythologIQ-Labs-LLC/agent-memory), a public reference architecture for governed memory in autonomous systems, including PAMA, lifecycle, conformance, forgetting, provenance, and runtime evidence.
- **Production agent systems:** Bicameral, where I work across governed local-first agent runtime, MCP, evidence ingestion, authority boundaries, deterministic validation, and release evidence.
- **Independent implementation:** MythologIQ Labs systems spanning deterministic governance, governed software production, local inference, privacy, memory, and agent-development infrastructure.

## Selected contributions

These links are intentionally specific. They show implementation context, review history, and evidence rather than asking a profile paragraph to do all the convincing.

| Area | Contribution | Evidence |
| --- | --- | --- |
| **Agent Memory ↔ AgenTrust** | Defined the portable memory-governance evidence wedge: Agent Memory owns memory semantics/PAMA/lifecycle while AgenTrust-compatible systems attest to integrity, execution, correlation, and portable verification. The reference scenario distinguishes a valid `DEL` from complete forgetting. | [Issue #63](https://github.com/MythologIQ-Labs-LLC/agent-memory/issues/63) · [ADR-021](https://github.com/MythologIQ-Labs-LLC/agent-memory/blob/main/docs/adr/ADR-021-portable-memory-governance-evidence-boundary.md) |
| **AgenTrust · Agent Manifest** | Designed the v0.2 incremental memory checkpoint/delta binding protocol for governed persistent agent memory, using RFC 9162 consistency proofs and fail-closed drift semantics. | [Issue #174](https://github.com/agentrust-io/agent-manifest/issues/174) · [PR #190](https://github.com/agentrust-io/agent-manifest/pull/190) |
| **Agent Memory** | Authored a public governed-memory reference architecture separating probabilistic epistemics from bounded consequence authority, with 19 accepted ADRs, PAMA doctrine, validated conformance fixtures, and a runtime-evidence program. | [Repository](https://github.com/MythologIQ-Labs-LLC/agent-memory) · [Runtime evidence](https://github.com/MythologIQ-Labs-LLC/agent-memory/blob/main/docs/programs/runtime-evidence/README.md) |
| **Microsoft AGT** | Governed accumulated context across delegated multi-agent workflows. | [PR #2800](https://github.com/microsoft/agent-governance-toolkit/pull/2800) |
| **Microsoft AGT** | Hardened contributor-reputation heuristics for organizational and domain-specialist contributors. | [PR #2852](https://github.com/microsoft/agent-governance-toolkit/pull/2852) |
| **Microsoft AGT** | MCP trust-verification integration guidance and reference implementation. | [PR #747](https://github.com/microsoft/agent-governance-toolkit/pull/747) |
| **Bicameral** | Built a provider-neutral ingestion path with GitHub reference acquisition, security screening, evidence identity, and lifecycle tracing. | [Integrations PR #255](https://github.com/BicameralAI/bicameral-integrations/pull/255) |
| **Bicameral** | Implemented governed real-data conformance and redaction evidence with tamper-evident transformation lineage and fail-closed handling. | [Integrations PR #269](https://github.com/BicameralAI/bicameral-integrations/pull/269) |
| **Bicameral** | Added deterministic validation and decision-evidence gates for adversarial redaction-backend evaluation. | [Integrations PR #287](https://github.com/BicameralAI/bicameral-integrations/pull/287) |

[**View the broader technical-work index →**](PUBLIC_WORK.md)

## Agent Memory: current wedge into AgenTrust

[Agent Memory](https://github.com/MythologIQ-Labs-LLC/agent-memory) now has a concrete interoperability path into the AgenTrust ecosystem rather than a generic adjacency claim.

```text
Agent Memory
  memory semantics · PAMA · lifecycle · canonical receipt
        |
        v
portable governance-evidence projection
        |
        v
AgenTrust / TRACE / Agent Manifest
  integrity · attestation · action correlation · portable verification
```

The core distinction is deliberate:

```text
integrity of mutation
        !=
semantic authorization of mutation
        !=
lifecycle obligation satisfaction
```

The first reference scenario is deletion completeness. An Agent Manifest checkpoint may validly prove that `DEL(memory-123)` occurred and that checkpoint `N -> N+1` verifies. Agent Memory can simultaneously prove that the delete was authorized **and** that a derived embedding or projection still survives. In that case mutation integrity passes while forgetting remains incomplete.

The public technical-artifact direction is correspondingly narrow: **“A Deletion Is Not a DEL: Verifiable Semantic Governance for Agent Memory.”**

The preferred upstream path begins with an AgenTrust integration/conformance surface, not a premature core-spec change. The goal is interoperability without moving PAMA or Agent Memory lifecycle semantics into TRACE or Agent Manifest.

## Selected public systems

| Project | Role / relevance |
| --- | --- |
| **[Agent Memory](https://github.com/MythologIQ-Labs-LLC/agent-memory)** | Governed-memory reference architecture with PAMA, lifecycle, forgetting, conformance, runtime evidence, and an explicit AgenTrust interoperability wedge. |
| **[Agent Governance Toolkit](https://github.com/microsoft/agent-governance-toolkit)** | Maintainer / contributor to open governance infrastructure for autonomous agents. |
| **[Agent Manifest](https://github.com/agentrust-io/agent-manifest)** | Contributor to verifiable agent identity/state specification and SDK behavior. |
| **[Bicameral Integrations](https://github.com/BicameralAI/bicameral-integrations)** | Publicly inspectable Bicameral work: acquisition, normalization, redaction, provenance, evidence, and governed evaluation. |
| **[FailSafe](https://github.com/MythologIQ-Labs-LLC/FailSafe)** | MythologIQ deterministic governance layer for accountable agent execution. |
| **[Qor-Logic](https://github.com/MythologIQ-Labs-LLC/Qor-logic)** | Governance framework for agent-driven software development and evidence-bound workflows. |
| **[presidio-rs](https://github.com/MythologIQ-Labs-LLC/presidio-rs)** | Rust-oriented privacy and redaction infrastructure. |
| **[GG-CORE](https://github.com/MythologIQ-Labs-LLC/GG-CORE)** | Local inference runtime and integration surface. |

## Authored private systems and professional implementation

Some substantial implementation remains private. These are authored systems or professional work, while the public repositories above provide independently inspectable evidence.

| System | What I authored / implemented |
| --- | --- |
| **FailSafe Pro** *(private)* | Governed software-production system built around a deterministic Rust governance kernel, capability mediation, governed MCP, Merkle/HMAC audit, approval and break-glass controls, evidence compilation, release governance, and runtime observation. |
| **Qor-logic-plus** *(private)* | Enterprise governance/control-plane extension covering organization policy inheritance, actor trust classification, manifests, evidence obligations, deployment receipts, instruction-file governance, release sequencing, and organization oversight. |
| **COREFORGE** *(private)* | Local-first multi-agent desktop system combining encrypted memory, policy-governed actions, orchestration, local inference, permissions, plugin boundaries, and user-controlled autonomy. |
| **Bicameral runtime / MCP** *(private)* | Production runtime and MCP work involving session-scoped authority, exact identity binding, replay/currentness checks, atomic decision promotion, bounded confirmation, stable-ID selection, and explicit human/product authority boundaries. |

The distinction is **visibility, not authorship**. Private source access limits independent inspection, not the relevance of the work.

## Engineering focus

<table>
<tr>
<td width="50%" valign="top">

### Governance and authority

- Deterministic policy enforcement
- Fail-closed security boundaries
- Capability and authority mediation
- PAMA and proportional mutation authority
- Human approval and confirmation contracts
- Spec-to-runtime conformance
- Agent and contributor trust models

</td>
<td width="50%" valign="top">

### Evidence and state

- Provenance and transformation lineage
- Tamper-evident audit structures
- Persistent agent memory governance
- Correction, deletion, forgetting, and residue
- Replay, currentness, and idempotency
- Adversarial and negative-path testing
- Evidence-bound release controls

</td>
</tr>
</table>

## Operating principles

1. **Uncertainty may propose. Authority constrains.** Probabilistic inference is useful; durable consequences require bounded permission.
2. **Deny by default.** Authority is earned for the action being attempted, not inherited from a vague session-level trust state.
3. **Provenance over phrasing.** Where an instruction, artifact, memory, or decision came from matters more than how confidently it is worded.
4. **Stable identity over presentation.** IDs, digests, specifications, and exact state bind authority. Display order and prose do not.
5. **Negative paths are part of the contract.** A system is not governed if stale state, replay, residual data, partial failure, or unauthorized mutation are undefined.
6. **Evidence should outlive the agent.** Important decisions need inspectable artifacts, not a claim that the model considered them.

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

[LinkedIn](https://www.linkedin.com/in/kevin-r-knapp/) · [MythologIQ Labs](https://www.linkedin.com/company/mythologiq/) · [Bicameral](https://www.linkedin.com/company/bicameral-ai/) · [Technical Work](PUBLIC_WORK.md)

</div>