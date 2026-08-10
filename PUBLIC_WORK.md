# Technical work

This index is a curated evidence surface for my work in agent governance, verifiable AI systems, governed software delivery, privacy, local-first agent infrastructure, and governed agent memory.

It distinguishes between **publicly inspectable evidence** and **authored private systems**. Public issues, pull requests, and repositories are linked directly. Private systems are described separately because lack of public source access changes inspectability, not authorship.

## Publicly inspectable work

## AgenTrust

### Agent Manifest

**Governed persistent-memory checkpointing**  
Designed the v0.2 memory checkpoint/delta binding protocol for persistent agent state, using RFC 9162 append-only Merkle consistency proofs to permit bounded memory evolution while preserving fail-closed drift semantics.

- [Issue #174: Memory checkpoint/delta binding protocol](https://github.com/agentrust-io/agent-manifest/issues/174)
- [PR #190: implementation](https://github.com/agentrust-io/agent-manifest/pull/190)
- [Agent Manifest repository](https://github.com/agentrust-io/agent-manifest)

Focus: persistent state · Merkle consistency · drift detection · specification design · conformance

## Microsoft Agent Governance Toolkit

Selected contributions:

- [PR #2800: governed accumulated context across delegated workflows](https://github.com/microsoft/agent-governance-toolkit/pull/2800)  
  Context governance across multi-agent delegation, including inherited restrictions and sensitivity.

- [PR #2852: organization/domain-specialist contributor reputation](https://github.com/microsoft/agent-governance-toolkit/pull/2852)  
  Contributor trust and reputation semantics hardened for organization accounts and domain specialists.

- [PR #747: MCP trust-verification integration](https://github.com/microsoft/agent-governance-toolkit/pull/747)  
  Integration guidance and reference implementation for connecting MCP surfaces to trust verification.

- [PR #746: prompt-injection allowlist validation](https://github.com/microsoft/agent-governance-toolkit/pull/746)  
  Fail-closed validation for allowlisted inputs and prompt-injection resistance.

- [PR #752: EU AI Act capability and control-gap mapping](https://github.com/microsoft/agent-governance-toolkit/pull/752)  
  Mapping regulatory obligations into concrete governance capabilities and implementation gaps.

- [PR #745: OWASP LLM Top 10 mapping](https://github.com/microsoft/agent-governance-toolkit/pull/745)

- [PR #741: custom governance integrations tutorial](https://github.com/microsoft/agent-governance-toolkit/pull/741)

- [PR #738: governance visualization system](https://github.com/microsoft/agent-governance-toolkit/pull/738)

Repository: [microsoft/agent-governance-toolkit](https://github.com/microsoft/agent-governance-toolkit)

Focus: agent governance · trust models · delegated workflows · MCP · compliance-to-control translation · fail-closed enforcement

## Bicameral

I serve as Lead AI Product Engineer at Bicameral. Some runtime and MCP repositories are private, so the links below intentionally use the publicly inspectable `bicameral-integrations` repository as one evidence surface. My private Bicameral runtime and MCP work is described later in this document.

### Governed acquisition and evidence

- [PR #255: universal fail-open normalization and GitHub reference path](https://github.com/BicameralAI/bicameral-integrations/pull/255)  
  Provider-neutral observations, stable evidence identity, shared normalization, GitHub webhook/backfill acquisition, Linear integration, advisory-signal separation, and lifecycle tracing.

- [PR #269: real-data conformance harness and guarded redaction boundary](https://github.com/BicameralAI/bicameral-integrations/pull/269)  
  Tamper-evident stage and transformation lineage, deterministic redaction receipts, bounded process isolation, value-free failures, and explicit separation between evidence and release authority.

### Governed technical decision evidence

- [PR #281: candidate-neutral redaction backend evaluation contract](https://github.com/BicameralAI/bicameral-integrations/pull/281)  
  ADR and executable evaluation contract covering leakage, identity mutation, network behavior, determinism, cleanup, licensing, performance, and receipt compatibility without pre-selecting a backend.

- [PR #287: deterministic evaluation and decision-evidence gates](https://github.com/BicameralAI/bicameral-integrations/pull/287)  
  Offline corpus validation, artifact-digest checks, adversarial review contracts, owner-decision evidence, and fail-closed eligibility logic.

- [PR #292: hosted exact-head validation for stacked evaluation work](https://github.com/BicameralAI/bicameral-integrations/pull/292)  
  Exact-head CI evidence, committed artifact consistency checks, mutation tests, and bounded validation receipts.

### Runtime safety and integration boundaries

- [PR #232: aggregate response-byte cap across paginated polls](https://github.com/BicameralAI/bicameral-integrations/pull/232)
- [PR #231: authority-stripped external ingest emission](https://github.com/BicameralAI/bicameral-integrations/pull/231)
- [PR #234: guided connector configuration for Linear and Google Drive](https://github.com/BicameralAI/bicameral-integrations/pull/234)

Repository: [BicameralAI/bicameral-integrations](https://github.com/BicameralAI/bicameral-integrations)

Focus: evidence provenance · acquisition trust · PII redaction · authority separation · exact-head validation · adversarial review · governed delivery

## MythologIQ Labs

### FailSafe

[MythologIQ-Labs-LLC/FailSafe](https://github.com/MythologIQ-Labs-LLC/FailSafe)

Deterministic governance and accountable execution for autonomous agents, centered on enforceable policy, gated workflows, and verifiable evidence rather than prompt-only controls.

Focus: agent safety · deterministic governance · execution control · auditability

### Qor-Logic

[MythologIQ-Labs-LLC/Qor-logic](https://github.com/MythologIQ-Labs-LLC/Qor-logic)

Governance framework for agent-driven software development, including gated research/planning/review/implementation workflows, evidence requirements, and tamper-evident governance history.

Focus: governed SDLC · adversarial review · evidence gates · agent operating discipline

### presidio-rs

[MythologIQ-Labs-LLC/presidio-rs](https://github.com/MythologIQ-Labs-LLC/presidio-rs)

Rust-oriented privacy/redaction infrastructure exploring a native path for Presidio-style detection and anonymization workflows.

Focus: Rust · privacy · PII detection · redaction infrastructure

### GG-CORE

[MythologIQ-Labs-LLC/GG-CORE](https://github.com/MythologIQ-Labs-LLC/GG-CORE)

Local inference runtime work intended to support private, on-device model execution and consumption by higher-level agent systems.

Focus: local inference · runtime integration · privacy-preserving AI

### Additional public repositories

- [CodeGenome](https://github.com/MythologIQ-Labs-LLC/CodeGenome)
- [EvolveAI](https://github.com/MythologIQ-Labs-LLC/EvolveAI)
- [CritIQ](https://github.com/MythologIQ-Labs-LLC/CritIQ)
- [agent-failsafe](https://github.com/MythologIQ-Labs-LLC/agent-failsafe)

## Authored private systems and architecture

The systems below are part of my authored technical body of work. Their source is private, so they are not presented as independently inspectable evidence in the same way as the links above.

### Agent Memory

Canonical reference architecture that consolidates governed-memory concepts across systems I authored, including UOR, EvolveAI, CodeGenome, COREFORGE/Neurospace, PAMA, Qor/FailSafe, and related governance work.

The architecture treats agentic memory as governed state transition over addressable artifacts rather than simple retrieval. It defines:

- stable identity and addressability;
- evidence and provenance;
- relevance, saturation, decay, and lifecycle routing;
- mutation and promotion authority;
- crystallization and certification;
- source trust and conflict resolution;
- temporal causality;
- privacy and sensitivity classification;
- governed recall and context assembly;
- schema evolution;
- retention, deletion, and tombstones;
- actor scope, consent, and tenancy;
- audit events;
- recovery, rollback, and replay;
- memory quality metrics;
- conformance and calibration fixtures;
- multi-agent shared-memory boundaries.

Focus: governed memory · mutation authority · provenance · certification · conformance · replay · privacy · multi-agent state

### FailSafe Pro

Private governed software-production system centered on deterministic enforcement rather than prompt compliance.

Key authored surfaces include a Rust governance kernel, typed policy evaluation, capability brokerage for filesystem/git/shell/deployment operations, governed MCP tooling, Merkle/HMAC audit structures, approval and break-glass controls, evidence compilation, release governance, observation/anomaly handling, federation, and local-review integration.

Focus: deterministic governance · capability mediation · auditability · governed MCP · software-production controls

### Qor-logic-plus

Private enterprise extension of Qor-Logic that adds higher-tier governance control-plane capabilities over the public framework.

Key authored surfaces include organization policy inheritance, actor trust classification, governance manifests, evidence obligations, deployment receipts, instruction-file governance, release sequencing, cross-repository oversight, and conformance-oriented enforcement.

Focus: enterprise governance · trust classification · policy inheritance · deployment evidence · organization oversight

### COREFORGE

Private local-first multi-agent desktop system integrating governed autonomy with user-owned context and local execution.

Key authored surfaces include encrypted memory, orchestration, local inference, authentication and permission boundaries, governed actions, plugin/runtime controls, and explicit approval surfaces.

Focus: local-first agents · encrypted memory · orchestration · permissions · governed autonomy

### Bicameral runtime and MCP work

Private professional implementation work includes authority- and state-sensitive runtime behavior such as session-scoped candidate state, process-scoped capabilities, exact identity binding, replay/currentness checks, deterministic decision identities, atomic promotion, bounded confirmation, dependency closure, and explicit separation between agent transport and human/Product authority.

Focus: authority boundaries · MCP · deterministic state transitions · exact binding · atomicity · replay · human confirmation

## Working themes

Across these projects, the recurring engineering questions are the same:

1. What entity actually has authority to mutate state?
2. How is that authority bound to identity, scope, version, and current state?
3. What evidence proves the operation was valid after the agent process is gone?
4. What happens under stale state, replay, partial failure, ambiguous provenance, or adversarial input?
5. Can a human, verifier, or independent implementation reproduce the result without trusting model prose?

Those questions are the center of my work in agent governance and verifiable AI systems.