---
title: "DOHNUT Commerce + Creative OS System Index"
date: "2026-08-31"
version: "1.2.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "approved"
tags: [index, architecture, ecommerce, ai, governance, visual-benchmark, erp]
related_documents:
  - "../README.md"
  - "../PRD.md"
  - "../ARCHITECTURE.md"
  - "../DESIGN.md"
  - "../ERP.md"
  - "../PROMPT.md"
  - "../INTEGRATION-E-COMMERCE.md"
  - "./brand/brand-constitution-v1.0.0.md"
  - "./creative/doh-language-v1.0.0.md"
  - "./creative/doh-cinema-v1.0.0.md"
  - "./creative/doh-boy-v1.0.0.md"
  - "./creative/pop-culture-playbook-v1.0.0.md"
  - "./visual-ai/visual-ai-engine-v1.0.1.md"
  - "./visual-ai/dohnut-visual-benchmark-v1.0.0.md"
  - "./visual-ai/creative-genome-v1.0.0.md"
  - "./visual-ai/google-flow-prompt-template-v1.0.0.md"
  - "./ai/prompt-system-v1.0.0.md"
  - "./ai/provider-architecture-v1.0.0.md"
  - "./ai/skills-matrix-v1.0.0.md"
  - "./schemas/data-contracts-v1.0.0.md"
  - "./schemas/asset-registry-v1.0.0.md"
  - "./governance/governance-v1.0.0.md"
  - "./governance/source-of-truth-hierarchy-v1.0.0.md"
  - "./governance/quality-gates-v1.0.0.md"
  - "./governance/markdown-authoring-standard-v1.0.0.md"
---

# DOHNUT Commerce + Creative OS System Index

## 1. Objective

Satu **operating model** untuk menyambungkan brand truth, creative intelligence, AI generation, ecommerce, operations/ERP dan customer feedback tanpa kehilangan traceability.

## 2. Master Development Documents

| **Document** | **Purpose** |
| --- | --- |
| [PRD](../PRD.md) | Product scope, requirements, users and acceptance criteria |
| [ARCHITECTURE](../ARCHITECTURE.md) | Technical boundaries, services, data and integration |
| [DESIGN](../DESIGN.md) | UI/UX, Figma, visual system and experience flows |
| [ERP](../ERP.md) | Inventory, production, procurement, fulfilment and finance |
| [PROMPT](../PROMPT.md) | Prompt contracts, routing and AI execution |
| [Ecommerce Integration](../INTEGRATION-E-COMMERCE.md) | DOHNUT-Creative-OS ↔ Dowgnut-Custom contract |

## 3. Source of Truth

Rujuk [Source of Truth Hierarchy](./governance/source-of-truth-hierarchy-v1.0.0.md). Higher-level constraints sentiasa mengatasi lower-level experiments.

## 4. System Architecture

```text
BRAND TRUTH
    ↓
VISUAL BENCHMARK
    ↓
CONTROLLED GLOSSARY
    ↓
CREATIVE GENOME
    ↓
DOH LANGUAGE™ ── DOH CINEMA™ ── DOH BOY™
    ↓
POP CULTURE ADAPTER
    ↓
PROMPT COMPILER
    ↓
PROVIDER ADAPTER
    ↓
TEXT / IMAGE / VIDEO GENERATION
    ↓
QUALITY GATES
    ↓
ASSET REGISTRY
    ↓
PERFORMANCE + LEARNING
    ↓
CREATIVE MEMORY
    │
    ▼
ECOMMERCE / ERP
```

## 5. Repository Model

```text
DOHNUT-Creative-OS
        │
        │ canonical creative intelligence
        ▼
Dowgnut-Custom
        │
        │ commerce application runtime
        ▼
Customer Experience
```

The target is integration by contract, not a blind file merge.

## 6. Module Map

| **ID** | **Module** | **Output** | **Independent?** |
| --- | --- | --- | --- |
| MOD-01 | Brand Constitution | brand truth | Ya |
| MOD-02 | DOH Language | puns, hooks, copy | Ya |
| MOD-03 | DOH Cinema | cinematic concepts | Ya |
| MOD-04 | Doh Boy | character behaviour/copy | Ya |
| MOD-05 | Pop Culture Adapter | transformed references | Ya |
| MOD-06 | Visual Benchmark | visual reference | Ya |
| MOD-07 | Creative Genome | structured creative brief | Ya |
| MOD-08 | Visual AI Engine | production prompts | Bergantung pada genome + benchmark |
| MOD-09 | Prompt System | reusable task prompts | Ya |
| MOD-10 | Provider Architecture | routing + fallback | Ya |
| MOD-11 | Skills | capability requirements | Ya |
| MOD-12 | Governance + QA | rules + scoring | Ya |
| MOD-13 | Asset Registry | provenance + lineage | Ya |
| MOD-14 | Commerce Integration | ecommerce contract | Bergantung pada app repo |
| MOD-15 | ERP | business operations | Bergantung pada commerce |

## 7. Recommended Execution Order

### Phase 1 — Truth

1. Lock brand constitution and glossary.
2. Lock visual benchmark and approved assets.
3. Apply source-of-truth precedence.

### Phase 2 — Creative

4. Validate DOH Language.
5. Validate DOH Cinema.
6. Lock Doh Boy canon.
7. Maintain Pop Culture Playbook.

### Phase 3 — Commerce Foundation

8. Integrate ecommerce product contracts.
9. Implement catalogue, product, DOH Box, checkout and orders.
10. Connect approved creative assets.

### Phase 4 — AI Production

11. Validate Creative Genome.
12. Compile prompts.
13. Apply provider adapter/fallback.
14. Generate and QA.
15. Register asset lineage.

### Phase 5 — ERP

16. Inventory.
17. Production.
18. Procurement.
19. Fulfilment.
20. Reconciliation/reporting.

### Phase 6 — Learning

21. Capture performance.
22. Update Creative Memory.
23. Improve routing and quality rules.

## 8. Quality Definition

Ready means:
- Brand Truth pass.
- Visual benchmark pass when applicable.
- Product/operational facts pass.
- Platform fit pass.
- IP/cultural/safety pass.
- Metadata/version pass.
- Human approval when required.

## 9. Definition of Done

- [ ] Requirement mapped.
- [ ] UX mapped to Figma.
- [ ] Architecture boundary documented.
- [ ] Data contract exists where required.
- [ ] Prompt/skill references valid.
- [ ] QA gate mapped.
- [ ] Asset lineage available.
- [ ] Ecommerce/ERP authority rules respected.
- [ ] Changelog updated.
- [ ] Main branch contains the canonical change.
