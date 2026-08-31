---
title: "DOHNUT Creative Genome"
date: "2026-08-31"
version: "1.0.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "draf"
tags: [creative-genome, schema, prompt-compiler, visual-ai]
related_documents:
  - "./visual-ai-engine-v1.0.0.md"
  - "../creative/doh-language-v1.0.0.md"
  - "../creative/doh-cinema-v1.0.0.md"
  - "../creative/doh-boy-v1.0.0.md"
---

# DOHNUT Creative Genome

## 1. Purpose

Creative Genome ialah structured brief object untuk memastikan setiap AI generation mempunyai context, lineage dan parameter yang boleh diaudit.

## 2. Schema

```json
{
  "objective": "limited_drop_campaign",
  "audience": "gen-z-young-millennials",
  "platform": "instagram-reels",
  "product": {
    "type": "stuffed_donut",
    "flavour": "chocolate_hazelnut",
    "filling_behavior": "dramatic_ooze"
  },
  "visual": {
    "tier": 5,
    "camera": "low_angle_cinematic",
    "lighting": "premium_dramatic",
    "background": "dohnut_yellow"
  },
  "verbal": {
    "primary_line": "DOH WICK — THE LAST BITE"
  },
  "cinema": {
    "enabled": true,
    "genre": "action"
  },
  "character": {
    "enabled": true,
    "mode": "action_hero"
  },
  "references": [],
  "constraints": [
    "original_execution",
    "no_asset_cloning"
  ]
}
```

## 3. Required fields

| Field | Requirement |
| --- | --- |
| objective | Wajib |
| product.type | Wajib untuk food visual |
| product.flavour | Wajib jika flavour-specific |
| platform | Wajib untuk social output |
| visual.tier | Wajib |
| constraints | Wajib |

## 4. Missing input behavior

Jika field kritikal tiada, compiler mesti return `blocked` dan menyenaraikan `missing_inputs`. Jangan invent data produk.

## 5. Lineage

Setiap generated asset patut menyimpan:

- genome version
- prompt version
- module versions
- model/provider
- generation timestamp
- reviewer
- QA status
