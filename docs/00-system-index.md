---
title: "DOHNUT Creative OS System Index"
date: "2026-08-31"
version: "1.0.1"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "draf"
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
  - "./ai/prompt-system-v1.0.0.md"
  - "./ai/skills-matrix-v1.0.0.md"
  - "./schemas/data-contracts-v1.0.0.md"
  - "./governance/governance-v1.0.0.md"
---

# DOHNUT Creative OS System Index

## 1. Objective

Membina satu **creative operating system** yang memastikan setiap idea, prompt, visual, campaign dan asset boleh dihasilkan secara scalable sambil mengekalkan identiti DOHNUT.

## 2. Core architecture

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

## 3. Module map

| ID | Module | Output | Independent? |
| --- | --- | --- | --- |
| MOD-01 | Brand Constitution | brand truth | Ya |
| MOD-02 | DOH Language | puns, hooks, copy | Ya |
| MOD-03 | DOH Cinema | cinematic concepts | Ya |
| MOD-04 | Doh Boy | character behaviour/copy | Ya |
| MOD-05 | Pop Culture Adapter | transformed references | Ya |
| MOD-06 | Visual Benchmark | visual quality reference | Ya |
| MOD-07 | Visual AI Engine | production prompts | Bergantung pada genome + benchmark |
| MOD-08 | Prompt System | reusable task prompts | Ya |
| MOD-09 | Skills | capability requirements | Ya |
| MOD-10 | Governance + QA | rules, scores + fixes | Ya |

## 4. Recommended execution order

### Phase 1 — Truth

1. Lock brand constitution.
2. Lock glossary.
3. Lock visual benchmark and approved assets.

### Phase 2 — Creative language

4. Load DOH Language.
5. Load DOH Cinema.
6. Load Doh Boy canon.
7. Load Pop Culture Playbook.

### Phase 3 — AI production

8. Use Creative Genome schema.
9. Apply Visual Benchmark.
10. Select prompt(s) by deliverable.
11. Compile provider-specific prompt.
12. Generate.

### Phase 4 — QA and learning

13. Run brand, product, technical and IP QA.
14. Approve or revise.
15. Register asset lineage.
16. Capture performance feedback.

## 5. Quality definition

Sesuatu asset dianggap ready apabila:

- Brand Truth pass.
- Visual benchmark pass.
- Product fidelity pass.
- Visual/copy quality pass.
- Platform suitability pass.
- IP/cultural safety pass.
- Metadata and version pass.
- Human owner approval pass apabila diperlukan.

## 6. 30-60-90 day roadmap

| Period | Fokus | Deliverables |
| --- | --- | --- |
| 0-30 | Foundation | constitution, glossary, benchmark, genome, prompt registry |
| 31-60 | Creative engine | DOH modules, playbook, visual compiler, QA |
| 61-90 | Operations | asset registry, metrics, automation, regression tests |

## 7. Definition of Done

- [ ] Front matter lengkap.
- [ ] Semver valid.
- [ ] Cross-reference valid.
- [ ] Inputs dan outputs jelas.
- [ ] Constraints dinyatakan.
- [ ] Examples tersedia untuk tugas kompleks.
- [ ] Visual benchmark applied where relevant.
- [ ] QA gate dipetakan.
- [ ] Changelog dikemas kini.
