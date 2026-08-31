---
title: "DOHNUT Asset Registry Contract"
date: "2026-08-31"
version: "1.0.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "approved"
tags: [assets, registry, schema, provenance, lineage]
related_documents:
  - "./data-contracts-v1.0.0.md"
  - "../visual-ai/creative-genome-v1.0.0.md"
  - "../governance/quality-gates-v1.0.0.md"
---

# DOHNUT Asset Registry Contract

## 1. Purpose

Asset Registry ialah source of record untuk setiap output yang dihasilkan atau diluluskan oleh DOHNUT Creative OS.

## 2. Required fields

| **Field** | **Required** | **Purpose** |
| --- | --- | --- |
| `asset_id` | Yes | Unique identifier |
| `version` | Yes | Asset version |
| `asset_type` | Yes | image, video, copy, packaging, etc. |
| `campaign_id` | Conditional | Campaign lineage |
| `genome_id` | Conditional | Creative Genome reference |
| `prompt_id` | Conditional | Prompt provenance |
| `generator` | Yes | Provider/tool used |
| `model` | Conditional | Model identifier |
| `status` | Yes | draft, review, approved, rejected, deprecated |
| `created_at` | Yes | ISO-8601 timestamp |
| `owner` | Yes | Responsible person/team |
| `source` | Yes | Reference/source location |
| `ip_risk` | Yes | low, medium, high |
| `qa_result` | Yes | Gate scores/result |

## 3. Example

```yaml
asset_id: ASSET-2026-CH-001
version: 1.0.0
asset_type: hero-image
campaign_id: CAMP-CH-001
genome_id: GENOME-CH-001
prompt_id: VIS-PRODUCT-HERO-001
generator: google-flow
model: provider-model-id
status: approved
created_at: 2026-08-31T21:00:00+08:00
owner: creative-team
source: assets/benchmarks/chocolate-hazelnut
ip_risk: low
qa_result:
  brand: 2
  product: 2
  ip: 2
  platform: 2
```

## 4. Creative lineage

```text
BRIEF → GENOME → PROMPT → MODEL → OUTPUT → QA → APPROVAL → PUBLICATION → PERFORMANCE
```

## 5. Retention rule

Approved assets mesti kekal traceable kepada prompt, genome dan source reference. Jangan overwrite historical lineage; create new versions.
