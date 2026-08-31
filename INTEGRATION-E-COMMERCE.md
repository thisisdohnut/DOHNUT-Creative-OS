---
title: "DOHNUT Commerce Integration Contract — Dowgnut-Custom"
date: "2026-08-31"
version: "1.0.0"
author: "DOHNUT / GangNiaga Sdn. Bhd."
status: "draf"
tags: [integration, ecommerce, dowgnut-custom, creative-os, api, contracts]
related_documents: ["./README.md", "./PRD.md", "./ARCHITECTURE.md", "./DESIGN.md", "./ERP.md", "./PROMPT.md"]
---

# DOHNUT Commerce Integration Contract — Dowgnut-Custom

## 1. Objective

Dokumen ini menetapkan bahawa **Dowgnut-Custom** menjadi application/ecommerce implementation manakala **DOHNUT-Creative-OS** menjadi canonical creative/intelligence layer.

## 2. Repositories

| Repository | Role |
| --- | --- |
| `thisisdohnut/DOHNUT-Creative-OS` | Creative intelligence, brand truth, AI prompts, schemas, governance |
| `thisidowgnut-source/Dowgnut-Custom` | Ecommerce application, storefront, customer/order runtime |

## 3. Target State

```text
                    DOHNUT
                      │
          ┌───────────┴───────────┐
          ▼                       ▼
  CREATIVE INTELLIGENCE       COMMERCE APP
  DOHNUT-Creative-OS          Dowgnut-Custom
          │                       │
          └───────────┬───────────┘
                      ▼
              CUSTOMER EXPERIENCE
```

## 4. Integration Contract

### Creative OS → Commerce

- Approved image/video asset IDs.
- Approved campaign IDs.
- Approved copy variants.
- Product creative metadata.
- Visual benchmark references.

### Commerce → Creative OS

- Product ID.
- Product name.
- Canonical product attributes.
- Availability state.
- Campaign eligibility.
- Approved price only when explicitly marked canonical.

## 5. Authority Rules

| Data | Authority |
| --- | --- |
| Brand identity | Creative OS / Brand Constitution |
| Creative rules | Creative OS |
| AI prompt contracts | Creative OS |
| Product price | Commerce/ERP |
| Inventory | Commerce/ERP |
| Order state | Commerce/ERP |
| Payment state | Commerce/payment infrastructure |
| Customer PII | Commerce/customer domain |
| Published asset | Asset Registry + commerce/content runtime |

## 6. Recommended Technical Boundary

Preferred integration order:

1. Shared JSON schemas.
2. Versioned HTTP/API contract.
3. Event contract for asynchronous updates.
4. Asset storage references instead of binary duplication.
5. Optional reusable SDK/package after interfaces stabilise.

Do not import the full Creative OS documentation into application runtime.

## 7. Ecommerce Creative APIs

Illustrative endpoints:

```text
GET  /api/creative/products/:productId/context
POST /api/creative/briefs
POST /api/creative/generate
GET  /api/creative/assets/:assetId
POST /api/creative/qa
POST /api/creative/publish
```

Actual endpoints must be adapted to the existing Dowgnut-Custom framework.

## 8. Events

```text
product.updated
campaign.created
creative.asset.approved
creative.asset.published
order.created
order.paid
inventory.changed
creative.performance.recorded
```

## 9. Security

- Do not expose model provider secrets to the browser.
- Do not expose customer PII to creative prompts unless strictly required and authorised.
- Validate all asset URLs/IDs.
- Enforce RBAC for generation, approval and publication.
- Log critical actions.

## 10. Migration Strategy

### Stage 1 — Documentation contract

Align both repos on names, IDs, schemas and ownership.

### Stage 2 — Read-only integration

Commerce reads approved creative assets/metadata.

### Stage 3 — Creative write workflow

Commerce requests a brief/generation through an authenticated service boundary.

### Stage 4 — Publishing

Only approved assets can become public commerce content.

### Stage 5 — Learning

Ecommerce performance flows back to Creative Memory.

## 11. Current Access Limitation

The GitHub integration available in this workspace currently has **read-only access to `thisidowgnut-source/Dowgnut-Custom`**. Therefore this document establishes the integration contract in the Creative OS repository without modifying the source ecommerce repository.

To perform a real repository-to-repository code merge, the connected GitHub identity must have write access to the ecommerce repository.

## 12. Integration Definition of Done

- [ ] Both repositories recognise the same product/campaign/asset identifiers.
- [ ] Creative OS owns creative truth.
- [ ] Ecommerce owns commercial/order truth.
- [ ] Shared schemas are versioned.
- [ ] API/event boundaries are documented.
- [ ] Asset provenance is preserved.
- [ ] Sensitive data remains within authorised domains.
- [ ] Approved creative can be consumed by ecommerce.
- [ ] Performance can be returned to Creative OS.
