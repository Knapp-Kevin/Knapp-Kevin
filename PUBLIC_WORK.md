# Technical work

This index is a curated evidence surface for my work in agent governance, verifiable AI systems, governed software delivery, privacy, local-first agent infrastructure, and governed agent memory.

It distinguishes **publicly inspectable evidence** from private implementation. Public repositories, issues, pull requests, ADRs, and conformance artifacts are linked directly. Private systems are described separately because source visibility changes inspectability, not authorship.

## AgenTrust

### Agent Manifest

**Governed persistent-memory checkpointing**  
Designed the v0.2 memory checkpoint/delta binding protocol for persistent agent state, using RFC 9162 append-only Merkle consistency proofs to permit bounded memory evolution while preserving fail-closed drift semantics.

- [Issue #174: Memory checkpoint/delta binding protocol](https://github.com/agentrust-io/agent-manifest/issues/174)
- [PR #190: implementation](https://github.com/agentrust-io/agent-manifest/pull/190)
- [Agent Manifest repository](https://github.com/agentrust-io/agent-manifest)

Focus: persistent state · Merkle consistency · drift detection · specification design · conformance

### Agent Memory interoperability wedge

My public [Agent Memory](https://github.com/MythologIQ-Labs-LLC/agent-memory) project now defines a concrete, implementation-first interoperability boundary with the AgenTrust ecosystem.

- [Issue #63: Portable memory governance evidence for AgenTrust interoperability](https://github.com/MythologIQ-Labs-LLC/agent-memory/issues/63)
- [ADR-021: Portable Memory Governance Evidence Boundary](https://github.com/MythologIQ-Labs-LLC/agent-memory/blob/main/docs/adr/ADR-021-portable-memory-governance-evidence-boundary.md)
- [Runtime Evidence Program](https://github.com/MythologIQ-Labs-LLC/agent-memory/blob/main/docs/programs/runtime-evidence/README.md)

The ownership boundary is explicit:

```text
Agent Memory
  memory semantics + PAMA + lifecycle + canonical receipt
        |
        v
portable governance-evidence projection
        |
        v
AgenTrust / TRACE / Agent Manifest
  integrity + attestation + correlation + portable verification
```

The wedge is deliberately not “move Agent Memory into AgenTrust.” It tests whether semantic governance evidence can be independently verified without transferring ownership of memory semantics to the attestation layer.

The reference demonstration is deletion completeness:

```text
Agent Manifest / external evidence:
  DEL(memory-123) occurred
  checkpoint N -> N+1 is valid

Agent Memory:
  deletion was authorized
  derived embedding still survives

result:
  mutation integrity       PASS
  governance disposition   PASS
  forgetting completeness FAIL
```

The corresponding success case proves zero undeclared recoverable residue.

The public technical-artifact direction is:

**A Deletion Is Not a DEL: Verifiable Semantic Governance for Agent Memory**

Core claim:

> Proof that an authorized deletion operation occurred is not proof that the information was forgotten.

The preferred upstream sequence targets AgenTrust integration/conformance surfaces before proposing normative TRACE or Agent Manifest changes. Implementation evidence should expose any genuinely generic missing requirement first.

Focus: portable governance evidence · Agent Manifest checkpoints · TRACE-compatible action evidence · lifecycle verification · deletion completeness · privacy-preserving attestation

## Agent Memory

[MythologIQ-Labs-LLC/agent-memory](https://github.com/MythologIQ-Labs-LLC/agent-memory)

A public reference architecture for governed memory in autonomous and agentic systems.

The architecture treats agentic memory as retained state capable of altering future interpretation, reasoning, planning, tool use, action, or adaptation across a meaningful persistence boundary. It explicitly separates uncertain inference from consequence authority:

> **Probabilistic epistemics. Governed consequences.**  
> **Uncertainty may propose. Authority constrains.**

### Current architecture and evidence surfaces

- PAMA, Proportional Adaptive Mutation Authority, as native doctrine;
- explicit deterministic/probabilistic responsibility boundaries;
- memory lifecycle, correction, supersession, deletion, forgetting, and inheritance;
- provenance, source trust, temporal causality, sensitivity, tenancy, and recall admission;
- canonical versus derived-state semantics;
- conformance fixtures and calibration;
- 19 accepted architecture decisions with later runtime-evidence ADRs held Proposed until implementation earns acceptance;
- a runtime-evidence program that requires execution, pinning, reproducibility, negative paths, and reconstructable receipts;
- executable reference-adapter work against real memory substrates;
- a specific AgenTrust interoperability program through issue #63 and ADR-021.

Focus: governed memory · mutation authority · provenance · lifecycle · forgetting · conformance · runtime evidence · interoperability

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

I serve as Lead AI Product Engineer at Bicameral. Some runtime and MCP repositories are private, so the links below use the publicly inspectable `bicameral-integrations` repository as one evidence surface. Private runtime and MCP implementation is summarized later.

### Governed acquisition and evidence

- [PR #255: universal fail-open normalization and GitHub reference path](https://github.com/BicameralAI/bicameral-integrations/pull/255)  
  Provider-neutral observations, stable evidence identity, shared normalization, GitHub webhook/backfill acquisition, Linear integration, advisory-signal separation, and lifecycle tracing.

- [PR #269: real-data conformance harness and guarded redaction boundary](https://github.com/BicameralAI/bicameral-integrations/pull/269)  
  Tamper-evident stage and transformation lineage, deterministic redaction receipts, bounded process isolation, value-free failures, and explicit separation between evidence and release authority.

### Governed technical decision evidence

- [PR #281: candidate-neutral redaction backend evaluation contract](https://github.com/BicameralAI/bicameral-integrations/pull/281)
- [PR #287: deterministic evaluation and decision-evidence gates](https://github.com/BicameralAI/bicameral-integrations/pull/287)
- [PR #292: hosted exact-head validation for stacked evaluation work](https://github.com/BicameralAI/bicameral-integrations/pull/292)

### Runtime safety and integration boundaries

- [PR #232: aggregate response-byte cap across paginated polls](https://github.com/BicameralAI/bicameral-integrations/pull/232)
- [PR #231: authority-stripped external ingest emission](https://github.com/BicameralAI/bicameral-integrations/pull/231)
- [PR #234: guided connector configuration for Linear and Google Drive](https://github.com/BicameralAI/bicameral-integrations/pull/234)

Repository: [BicameralAI/bicameral-integrations](https://github.com/BicameralAI/bicameral-integrations)

Focus: evidence provenance · acquisition trust · PII redaction · authority separation · exact-head validation · adversarial review · governed delivery

## MythologIQ Labs public systems

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

## Authored private systems and professional implementation

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
4. What happens under stale state, replay, partial failure, ambiguous provenance, residual data, or adversarial input?
5. Can a human, verifier, or independent implementation reproduce the result without trusting model prose?

Those questions are the center of my work in agent governance and verifiable AI systems.