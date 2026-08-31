---
title: "DOHNUT Commerce + Creative OS — Architecture"
date: "2026-08-31"
version: "1.0.0"
author: "DOHNUT / GangNiaga Sdn. Bhd."
status: "draf"
tags: [architecture, ecommerce, creative-os, ai, erp, integration]
related_documents: ["./README.md", "./PRD.md", "./DESIGN.md", "./ERP.md", "./PROMPT.md"]
---

# DOHNUT Commerce + Creative OS — Architecture

## 1. Purpose

Dokumen ini mentakrifkan boundary teknikal untuk menggabungkan **DOHNUT-Creative-OS** dengan aplikasi ecommerce **Dowgnut-Custom** tanpa mencampurkan business truth, creative truth dan application runtime secara tidak terkawal.

## 2. System of Systems

```text
                    DOHNUT ECOSYSTEM
                           │
          ┌────────────────┴────────────────┐
          ▼                                 ▼
   CUSTOMER COMMERCE                  CREATIVE STUDIO
   Dowgnut-Custom                    DOHNUT Creative OS
          │                                 │
          └──────────────┬──────────────────┘
                         ▼
                  DOMAIN/API LAYER
                         │
             ┌───────────┼───────────┐
             ▼           ▼           ▼
          Commerce    Creative       ERP
             │           │           │
             └───────────┼───────────┘
                         ▼
                  DATA/EVENT LAYER
                         │
             ┌───────────┼───────────┐
             ▼           ▼           ▼
          Database    Asset Store  Analytics
```

## 3. Repository Boundary

### 3.1 DOHNUT-Creative-OS

Canonical source untuk:
- Brand Constitution.
- DOH Language™.
- DOH Cinema™.
- Doh Boy™.
- Pop Culture Playbook™.
- Visual Benchmark.
- Creative Genome.
- Prompt contracts.
- AI skills.
- Governance dan quality gates.
- Creative Memory definitions.

### 3.2 Dowgnut-Custom

Application/ecommerce source untuk:
- storefront.
- product browsing.
- cart/DOH Box.
- checkout.
- customer account.
- orders.
- admin/operator UI.
- runtime integrations.

Repo tersebut ialah existing application source dan mempunyai antara lain `brand-system`, `agent-ctx`, `Caddyfile`, environment example, deployment documentation dan lockfile; integration perlu mengekalkan existing runtime sebelum refactor besar dibuat.

## 4. Source-of-Truth Hierarchy

```text
LEGAL / REGULATORY
        ↓
BRAND CONSTITUTION
        ↓
APPROVED DESIGN SYSTEM
        ↓
CREATIVE CANON
        ↓
CAMPAIGN
        ↓
CREATIVE GENOME
        ↓
PROMPT
        ↓
AI OUTPUT
```

Lower level tidak boleh override higher level.

## 5. Core Components

### 5.1 Experience Layer

- Storefront.
- Customer account.
- Creative Studio.
- Admin.
- Operations dashboard.

### 5.2 Application Services

- Authentication/authorisation.
- Product service.
- Cart service.
- Order service.
- Customer service.
- Campaign service.
- Creative service.
- Asset service.
- Inventory service.
- Reporting service.

### 5.3 Creative Runtime

```text
Brief
→ Context Loader
→ Brand Policy
→ Creative Genome
→ Module Router
→ Prompt Compiler
→ Provider Adapter
→ Generation
→ QA
→ Asset Registry
```

### 5.4 ERP Runtime

```text
Order / Demand
→ Inventory
→ Production
→ Procurement
→ Fulfilment
→ Reconciliation
→ Reporting
```

## 6. Data Domains

| Domain | Objects |
| --- | --- |
| Brand | BrandRule, Token, Glossary |
| Creative | Brief, Genome, Campaign, Concept |
| Prompt | Prompt, Template, ProviderAdapter |
| Asset | Asset, Version, Provenance, Approval |
| Commerce | Product, Variant, Cart, Order |
| Customer | Customer, Address, Preference |
| Inventory | StockItem, Location, Movement |
| Production | Recipe, BOM, Batch |
| Procurement | Supplier, PO, Receipt |
| Finance | Payment, Refund, Reconciliation |
| Analytics | Event, KPI, Experiment |

## 7. Integration Contract

### 7.1 Creative OS → Ecommerce

Allowed:
- approved asset IDs.
- campaign IDs.
- product creative metadata.
- approved copy variants.

Not allowed:
- direct mutation of financial truth.
- arbitrary product prices.
- inventory creation without commerce authority.

### 7.2 Ecommerce → Creative OS

Allowed:
- product ID/name.
- approved availability status.
- campaign eligibility.
- product facts explicitly marked canonical.

The creative layer must not infer unavailable facts.

## 8. Event Vocabulary

```text
product.updated
inventory.changed
order.created
order.paid
order.fulfilled
order.cancelled
campaign.created
creative.brief.created
creative.generated
creative.qa.failed
creative.approved
asset.published
creative.performance.recorded
```

Events should use versioned schemas when contracts change.

## 9. Provider Abstraction

```text
Creative Intent
      ↓
Provider Adapter Interface
 ┌────┼───────┐
 ↓    ↓       ↓
Image Video Other
```

Google Flow may be one adapter. Brand logic must not be hardcoded to one vendor.

## 10. Failure Handling

### Creative

```text
Primary Provider
→ Retry
→ Fallback Provider
→ Degraded Output
→ Human Escalation
```

### Commerce

```text
Request
→ Validation
→ Idempotency
→ Transaction
→ Event
→ Confirmation
```

Payment/order flows must be idempotent.

## 11. Security

- Least-privilege access.
- RBAC by role.
- Secrets outside repository.
- No API keys inside prompts.
- PII minimisation.
- Audit trail for approvals and financial actions.
- Explicit human approval for sensitive actions.

## 12. Observability

Track where applicable:
- request ID.
- actor ID.
- service.
- provider/model.
- prompt version.
- latency.
- result.
- error category.
- asset ID.

Do not log secrets or unnecessary PII.

## 13. Deployment Boundaries

```text
local
→ development
→ staging
→ production
```

Production data must not be copied to lower environments without approved controls.

## 14. Integration Strategy

The target state is an **integrated system of systems**, not a blind repository merge.

```text
DOHNUT-Creative-OS
        │
        │ API / package / schema contract
        ▼
Dowgnut-Custom
        │
        ▼
DOHNUT Ecommerce Experience
```

The implementation team should prefer a versioned API or shared schema package rather than copying the full Creative OS repository into the ecommerce application.

## 15. Architecture Acceptance Checklist

- [ ] Repository boundaries are explicit.
- [ ] Creative truth is canonical.
- [ ] Commerce remains authoritative for price/order/inventory.
- [ ] Provider-specific code is isolated.
- [ ] Events and APIs are versioned.
- [ ] Sensitive data is access-controlled.
- [ ] Failure and fallback are defined.
- [ ] Asset provenance is preserved.
