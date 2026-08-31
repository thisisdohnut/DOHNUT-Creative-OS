---
title: "DOHNUT Creative OS Governance"
date: "2026-08-31"
version: "1.0.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "draf"
tags: [governance, qa, versioning, glossary]
related_documents:
  - "./glossary-v1.0.0.md"
  - "./ip-and-parody-v1.0.0.md"
  - "../schemas/data-contracts-v1.0.0.md"
---

# DOHNUT Creative OS Governance

## 1. Documentation standard

Semua dokumen mesti mempunyai YAML front matter dengan `title`, `date`, `version`, `author`, `status`, `tags`, dan `related_documents`.

## 2. Naming

Gunakan lowercase kebanyakannya untuk machine-facing filenames: `prompt-...-v1.0.0.md`, `skill-...-v1.0.0.md`, `campaign-...-v1.0.0.md`.

## 3. Semantic versioning

- **MAJOR:** breaking change kepada architecture, contract atau meaning.
- **MINOR:** capability baharu yang backward-compatible.
- **PATCH:** typo, clarification atau non-semantic correction.

## 4. Quality gates

| Gate | Focus | Pass requirement |
| --- | --- | --- |
| QG-01 | Brand | konsisten dengan Brand Constitution |
| QG-02 | Factuality | fakta mempunyai sumber atau dilabel sebagai assumption |
| QG-03 | Originality/IP | tiada asset cloning; escalate apabila perlu |
| QG-04 | Culture | local references natural dan tidak merendahkan |
| QG-05 | Platform | format, hook, CTA sesuai channel |
| QG-06 | Packaging | claims/mandatory info disemak manusia |
| QG-07 | Data | schema, unit, tarikh dan calculation konsisten |
| QG-08 | Operations | owner, dependency, deadline dan risk jelas |
| QG-09 | Orchestration | prompt/skill selection tepat |
| QG-10 | Documentation | links, versions dan changelog selaras |

## 5. Release threshold

Asset tidak boleh publish jika QG-01, QG-03, QG-06 atau QG-07 gagal.

## 6. Human escalation

Wajib escalate untuk legal/trademark/copyright clearance, food safety/regulatory claims, sensitive customer data, material financial decisions, atau visual yang terlalu hampir dengan protected asset.
