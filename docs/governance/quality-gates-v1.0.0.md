---
title: "DOHNUT Quality Gates"
date: "2026-08-31"
version: "1.0.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "approved"
tags: [qa, quality-gates, governance, ai]
related_documents:
  - "./governance-v1.0.0.md"
  - "./markdown-authoring-standard-v1.0.0.md"
  - "../brand/brand-constitution-v1.0.0.md"
  - "../visual-ai/visual-ai-engine-v1.0.0.md"
---

# DOHNUT Quality Gates

## 1. Purpose

Quality Gates menukarkan prinsip governance kepada pemeriksaan yang boleh dilaksanakan sebelum dokumen, prompt, campaign atau asset dianggap **release-ready**.

## 2. Gate matrix

| **Gate** | **Area** | **Minimum pass** | **Block release?** |
| --- | --- | --- | --- |
| QG-01 | Brand | Consistent with approved Brand Constitution | Yes |
| QG-02 | Factuality | Claims supported or labelled as assumptions | No |
| QG-03 | IP / originality | No confusing cloning or false endorsement | Yes |
| QG-04 | Culture | Local references are contextual and respectful | No |
| QG-05 | Platform | Correct dimensions, format, copy density and CTA | No |
| QG-06 | Packaging / regulated copy | Mandatory claims and product info human-reviewed | Yes |
| QG-07 | Data | Schema, dates, units and calculations valid | Yes |
| QG-08 | Operations | Owner, dependencies, deadline and rollback path known | No |
| QG-09 | AI orchestration | Correct prompt and skill chain selected | No |
| QG-10 | Documentation | Links, metadata, version and changelog valid | Yes for docs |
| QG-11 | Visual benchmark | Can I Taste It? Can I Feel It? Can I Recognize It? | Yes for visual hero assets |

## 3. Scoring

Gunakan skala 0-2 untuk setiap gate yang berkaitan:

- **0 = Fail**
- **1 = Needs revision**
- **2 = Pass**

Release threshold:

- Semua blocking gates mesti **2**.
- Tiada gate boleh berada pada **0**.
- Gate bernilai **1** mesti mempunyai owner dan remediation note.

## 4. Visual benchmark rubric

### Can I Taste It?

- Dough looks edible and freshly prepared.
- Filling and topping have believable physical behaviour.
- Lighting communicates appetizing texture.

### Can I Feel It?

- Softness, roundness and materiality are visually legible.
- Tactile quality supports the brand without looking like plastic CGI.

### Can I Recognize It?

- Colour, composition and creative treatment feel like DOHNUT.
- The asset does not depend solely on the logo for brand recognition.

## 5. Escalation

Escalate to a human owner for trademark/copyright clearance, food-safety claims, regulatory statements, sensitive customer data, financial decisions or material uncertainty.

## 6. Release checklist

- [ ] All applicable QG scores recorded.
- [ ] Blocking gates pass.
- [ ] Reviewer/owner recorded.
- [ ] Asset lineage recorded where applicable.
- [ ] Final version assigned.
- [ ] Changelog updated.
