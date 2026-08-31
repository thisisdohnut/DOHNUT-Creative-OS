---
title: "DOHNUT Creative OS Data Contracts"
date: "2026-08-31"
version: "1.0.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "draf"
tags: [schema, json, yaml, data-contract]
related_documents:
  - "../visual-ai/creative-genome-v1.0.0.md"
  - "../ai/prompt-system-v1.0.0.md"
  - "../governance/governance-v1.0.0.md"
---

# DOHNUT Creative OS Data Contracts

## 1. Principle

Setiap modul menerima data secara eksplisit. Missing critical data mesti menyebabkan `blocked`, bukan invented assumption.

## 2. Brand brief

```yaml
brand: DOHNUT
company: GangNiaga Sdn. Bhd.
market: Malaysia
geography: KL / Selangor / Klang Valley
model: D2C
tagline: GOOD VIBE. GOOD DOH.
objective: string
audience: string
product: string
channel: string
creative_direction: string
references: []
constraints: []
```

## 3. Content brief

```yaml
content_type: string
platform: string
objective: awareness|engagement|conversion|retention
audience: string
product_context: string
cta: string
voice: string
references: []
constraints: []
```

## 4. Creative Genome

```json
{
  "objective": "",
  "audience": "",
  "platform": "",
  "product": {"type": "", "flavour": "", "filling_behavior": ""},
  "visual": {"tier": 1, "camera": "", "lighting": "", "background": ""},
  "verbal": {"primary_line": "", "secondary_line": ""},
  "cinema": {"enabled": false, "genre": ""},
  "character": {"enabled": false, "mode": ""},
  "references": [],
  "constraints": []
}
```

## 5. QA result

```json
{
  "asset_id": "string",
  "status": "pass|revise|blocked",
  "scores": {
    "brand": 0,
    "product": 0,
    "visual": 0,
    "platform": 0,
    "ip": 0,
    "technical": 0
  },
  "findings": [],
  "required_actions": [],
  "reviewer": "string",
  "version": "1.0.0"
}
```
