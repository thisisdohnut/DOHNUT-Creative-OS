---
title: "DOHNUT Source of Truth Hierarchy"
date: "2026-08-31"
version: "1.0.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "approved"
tags: [governance, source-of-truth, hierarchy, ai]
related_documents:
  - "../00-system-index.md"
  - "../brand/brand-constitution-v1.0.0.md"
  - "./governance-v1.0.0.md"
---

# DOHNUT Source of Truth Hierarchy

## 1. Rule

Apabila dua dokumen, prompt atau creative output bercanggah, sumber pada tahap lebih tinggi mempunyai precedence.

## 2. Precedence

| **Level** | **Source** | **Role** |
| --- | --- | --- |
| 0 | Legal / regulatory requirements | Non-negotiable constraints |
| 1 | Brand Constitution | Brand truth |
| 2 | Approved design / visual system | Approved visual expression |
| 3 | Creative canon | DOH Language, Doh Boy, DOH Cinema rules |
| 4 | Campaign system | Campaign-specific expression |
| 5 | Prompt / generation instructions | Execution instructions |
| 6 | Experiment | Unapproved exploration |

## 3. Override rule

Lower-level documents tidak boleh override higher-level constraints tanpa perubahan yang diluluskan pada source tersebut.

## 4. Status model

Gunakan state berikut:

```text
DRAFT → REVIEW → APPROVED → STABLE → DEPRECATED
```

`EXPERIMENTAL` boleh digunakan untuk idea yang sengaja belum masuk creative canon.

## 5. AI behaviour

AI mesti:

1. Check applicable higher-level sources first.
2. Resolve conflicts by precedence.
3. Preserve approved terminology.
4. Escalate ambiguous conflicts instead of silently inventing a resolution.
