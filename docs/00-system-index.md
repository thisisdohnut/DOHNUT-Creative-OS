---
title: "DOHNUT Creative OS System Index"
date: "2026-08-31"
version: "1.1.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "approved"
tags: [index, architecture, roadmap, ai, governance, visual-benchmark]
related_documents:
  - "../README.md"
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

# DOHNUT Creative OS System Index

## 1. Objective

Membina satu **creative operating system** yang memastikan setiap idea, prompt, visual, campaign dan asset boleh dihasilkan secara scalable sambil mengekalkan identiti DOHNUT.

## 2. Source of truth

Rujuk [Source of Truth Hierarchy](./governance/source-of-truth-hierarchy-v1.0.0.md) sebelum membuat perubahan. Higher-level constraints sentiasa mengatasi lower-level experiments.

## 3. Core architecture

```text
BRAND TRUTH
    ↓
VISUAL BENCHMARK
    ↓
CONTROLLED GLOSSARY
    ↓
CREATIVE GENOME
    ↓
┌──────────────┬──────────────┬──────────────┐
│ DOH LANGUAGE │ DOH CINEMA   │ DOH BOY      │
└──────────────┴──────────────┴──────────────┘
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
```

## 4. Module map

| **ID** | **Module** | **Output** | **Independent?** |
| --- | --- | --- | --- |
| MOD-01 | Brand Constitution | brand truth | Ya |
| MOD-02 | DOH Language | puns, hooks, copy | Ya |
| MOD-03 | DOH Cinema | cinematic concepts | Ya |
| MOD-04 | Doh Boy | character behaviour/copy | Ya |
| MOD-05 | Pop Culture Adapter | transformed references | Ya |
| MOD-06 | Visual Benchmark | visual quality reference | Ya |
| MOD-07 | Creative Genome | structured creative brief | Ya |
| MOD-08 | Visual AI Engine | production prompts | Bergantung pada genome + benchmark |
| MOD-09 | Prompt System | reusable task prompts | Ya |
| MOD-10 | Provider Architecture | routing + fallback | Ya |
| MOD-11 | Skills | capability requirements | Ya |
| MOD-12 | Governance + QA | rules, scores + fixes | Ya |
| MOD-13 | Asset Registry | provenance + lineage | Ya |

## 5. Recommended execution order

### Phase 1 — Truth

1. Lock brand constitution and glossary.
2. Lock visual benchmark and approved assets.
3. Apply source-of-truth precedence.

### Phase 2 — Creative language

4. Load DOH Language.
5. Load DOH Cinema.
6. Load Doh Boy canon.
7. Load Pop Culture Playbook.

### Phase 3 — AI production

8. Build or validate the Creative Genome.
9. Select prompt family.
10. Compile provider-neutral prompt core.
11. Apply provider adapter and fallback policy.
12. Generate.

### Phase 4 — QA and learning

13. Run visual benchmark and quality gates.
14. Approve or revise.
15. Register asset lineage.
16. Capture performance feedback.

## 6. Quality definition

Asset dianggap ready apabila:

- Brand Truth pass.
- Visual benchmark pass.
- Product fidelity pass.
- Visual/copy quality pass.
- Platform suitability pass.
- IP/cultural safety pass.
- Metadata and version pass.
- Human owner approval pass apabila diperlukan.

## 7. Definition of Done

- [ ] Front matter lengkap untuk machine-facing docs.
- [ ] Semver valid.
- [ ] Cross-reference valid.
- [ ] Inputs dan outputs jelas.
- [ ] Constraints dinyatakan.
- [ ] Examples tersedia untuk task kompleks.
- [ ] Visual benchmark applied where relevant.
- [ ] QA gate dipetakan.
- [ ] Asset lineage tersedia untuk generated/approved assets.
- [ ] Changelog dikemas kini.
