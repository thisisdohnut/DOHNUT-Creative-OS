---
title: "DOHNUT Commerce + Creative OS — Product Requirements Document"
date: "2026-08-31"
version: "1.0.0"
author: "DOHNUT / GangNiaga Sdn. Bhd."
status: "draf"
tags: [dohnut, prd, ecommerce, creative-os, ai, erp, product]
related_documents:
  - "./README.md"
  - "./ARCHITECTURE.md"
  - "./DESIGN.md"
  - "./ERP.md"
  - "./PROMPT.md"
---

# DOHNUT Commerce + Creative OS — Product Requirements Document

## 1. Executive Summary

DOHNUT Commerce + Creative OS ialah blueprint produk bersepadu untuk membina pengalaman **D2C ecommerce + Creative Studio + AI creative engine + operations/ERP**. Dokumen ini menjadi sumber requirement utama yang memetakan objektif perniagaan kepada pengalaman pelanggan, sistem operasi, data, AI dan acceptance criteria.

DOHNUT ialah Malaysian-born premium donut D2C brand di bawah GangNiaga Sdn. Bhd., dengan fokus awal KL/Selangor (Lembah Klang), model online-first dan delivery-led.

Prinsip produk:

> **GOOD VIBE. GOOD DOH.**

Prinsip visual:

> **REAL FOOD FIRST. PLAY SECOND. BRAND ALWAYS.**

## 2. Product Vision

Membina satu ekosistem digital di mana pelanggan boleh menemui dan membeli DOHNUT dengan friction minimum, manakala pasukan boleh merancang, menghasilkan, meluluskan, menerbitkan dan mengukur creative output melalui satu Creative OS yang berhubung terus dengan operasi ecommerce.

## 3. Strategic Objectives

### 3.1 Customer

- Kurangkan masa daripada landing ke checkout.
- Menjadikan produk mudah ditemui dan difahami.
- Berikan pengalaman brand yang konsisten pada setiap touchpoint.
- Sokong reorder dan retention.

### 3.2 Business

- Menjadikan ecommerce sebagai channel D2C utama.
- Memaksimumkan conversion dan repeat purchase.
- Membina first-party customer relationship.
- Menyediakan asas operasi yang boleh diskalakan.

### 3.3 Creative

- Kurangkan masa brief-to-asset.
- Gunakan canonical brand rules untuk semua creative.
- Simpan prompt, asset provenance, QA dan performance.
- Membolehkan experimentation tanpa merosakkan brand consistency.

### 3.4 AI

- Jadikan AI provider-independent di layer core.
- Gunakan structured prompts dan Creative Genome.
- Automasi kerja berulang tanpa membenarkan AI override brand/legal truth.
- Gunakan feedback untuk meningkatkan routing dan creative quality.

## 4. Product Boundaries

### 4.1 In Scope

- Public ecommerce storefront.
- Product catalogue.
- Product detail.
- Cart / DOH Box.
- Checkout dan order lifecycle.
- Customer account.
- Campaign landing pages.
- Creative Studio.
- Creative Genome.
- Prompt compilation.
- AI generation orchestration.
- Asset registry dan provenance.
- Quality gates.
- Inventory/production/procurement/fulfilment foundations.
- Analytics dan creative performance.

### 4.2 Out of Scope for Initial Release

- Full autonomous company management.
- Fully autonomous financial decisions.
- Replacement of regulated payment infrastructure.
- Replacement of all delivery providers.
- Foundation-model training from scratch.
- Unreviewed automated publishing of sensitive campaigns.

## 5. Users and Roles

| Role | Primary goals | Main modules |
| --- | --- | --- |
| Customer | Discover, buy, track, reorder | Ecommerce |
| Founder / Owner | Brand, business, approvals | All |
| Creative Lead | Campaigns and creative quality | Creative OS |
| Content Operator | Produce/adapt content | Creative Studio |
| Ecommerce Operator | Catalog, pricing, orders | Commerce |
| Operations | Stock, production, fulfilment | ERP |
| Finance | Payment and reporting control | ERP |
| Developer | Build/integrate services | Platform |
| AI Agent | Execute governed tasks | AI Runtime |

## 6. Product Modules

### 6.1 Customer Commerce

- Home / landing.
- Shop and category pages.
- Product detail.
- Search/filter.
- DOH Box / cart.
- Checkout.
- Order confirmation.
- Order tracking.
- Account.
- Reorder.
- Promotions.
- Campaign pages.

### 6.2 Creative Studio

- Dashboard.
- Brief Builder.
- Creative Genome.
- DOH Language™.
- DOH Cinema™.
- Doh Boy™.
- Pop Culture Playbook™.
- Visual AI Engine™.
- Prompt Builder.
- Generation history.
- QA.
- Asset Registry.
- Campaign management.
- Performance review.

### 6.3 Business Operations

- Product master.
- Inventory.
- Recipe/BOM.
- Production.
- Procurement.
- Orders.
- Fulfilment.
- Customers.
- Finance/reconciliation.
- Reporting.

## 7. Functional Requirements

### 7.1 Ecommerce Requirements

#### FR-E01 Product Catalogue

- Product CRUD.
- SKU and variant support.
- Price and status.
- Availability.
- Product imagery.
- Ingredients/allergens where applicable.
- Category and tag taxonomy.

#### FR-E02 Product Detail

Must provide:
- Product hero visual.
- Product name and description.
- Price.
- Availability.
- Quantity.
- Add to DOH Box CTA.
- Related products.
- Delivery/pickup information.
- Campaign context when relevant.

#### FR-E03 Cart / DOH Box

- Add/remove/update quantity.
- Inventory validation.
- Price calculation.
- Promotion calculation.
- Delivery/pickup selection.
- Persist cart state where applicable.

#### FR-E04 Checkout

- Customer information.
- Delivery/pickup.
- Payment method.
- Order review.
- Consent.
- Error recovery.
- Confirmation.

#### FR-E05 Customer Account

- Profile.
- Addresses.
- Order history.
- Reorder.
- Preferences.

### 7.2 Creative Requirements

#### FR-C01 Creative Brief

Input:
- objective
- audience
- product
- campaign
- platform
- format
- tone
- CTA
- references
- constraints

Output:
- validated Creative Genome.

#### FR-C02 Module Routing

Route a brief to one or more creative modules:
- DOH Language™.
- DOH Cinema™.
- Doh Boy™.
- Pop Culture Playbook™.
- Visual AI Engine™.

#### FR-C03 Prompt Compilation

Convert structured intent into a provider-neutral prompt contract and then into provider-specific syntax.

#### FR-C04 Generation

- Provider adapter.
- Request ID.
- Retry.
- Fallback.
- Output metadata.
- Cost/usage metadata where provider exposes it.

#### FR-C05 Quality Assurance

Mandatory checks:
- Brand.
- Product plausibility.
- Factuality.
- IP/parody.
- Cultural fit.
- Platform fit.
- Safety.
- Technical.

#### FR-C06 Asset Registry

Each approved asset must preserve:

```text
brief
→ genome
→ prompt
→ provider/model
→ output
→ QA
→ approval
→ publication
→ performance
```

### 7.3 Operations Requirements

- Product availability must flow to commerce.
- Order state must flow to fulfilment.
- Inventory reservation must occur before fulfilment commitment.
- Production output must update finished stock.
- Purchase receiving must update inventory.
- Financial actions must be auditable.

## 8. Critical User Journeys

### 8.1 Purchase Journey

```text
Landing
→ Browse
→ Product Detail
→ Add to DOH Box
→ Cart
→ Checkout
→ Payment
→ Confirmation
→ Fulfilment
→ Delivery / Pickup
→ Reorder
```

### 8.2 Creative Journey

```text
Brief
→ Creative Genome
→ Module Selection
→ Prompt Compilation
→ Provider
→ Generation
→ QA
→ Approval
→ Asset Registry
→ Publication
→ Performance
→ Creative Memory
```

### 8.3 Campaign Journey

```text
Objective
→ Audience
→ Product
→ Concept
→ DOH Language / Cinema / Doh Boy
→ Asset Pack
→ QA
→ Schedule
→ Publish
→ Measure
→ Learn
```

## 9. Data Requirements

Canonical entities:

| Entity | Required attributes |
| --- | --- |
| Product | id, sku, name, category, status |
| Variant | id, product_id, name, price, availability |
| Customer | id, contact, consent/status |
| Order | id, customer_id, totals, state |
| Inventory | sku, location, on_hand, reserved, available |
| Campaign | id, objective, audience, dates, status |
| Brief | id, campaign_id, objective, platform |
| Creative Genome | version, objective, modules, visual, copy |
| Prompt | id, version, input_contract, output_contract |
| Asset | id, type, source, lineage, status |
| QA Result | asset_id, checks, score, decision |

## 10. Non-Functional Requirements

| Area | Requirement |
| --- | --- |
| Performance | Responsive UI and predictable API latency |
| Availability | Graceful degradation for provider failures |
| Security | Least privilege and secret isolation |
| Privacy | Data minimisation and access controls |
| Accessibility | Keyboard, semantic labels, contrast and reduced-motion support |
| Auditability | Critical actions and creative lineage must be traceable |
| Maintainability | Modular boundaries and documented contracts |
| Portability | Core creative intent must remain provider-neutral |
| Observability | Logs, metrics and error classification |
| Versioning | Semantic versioning for docs/contracts |

## 11. Analytics and KPIs

### Commerce

- Conversion rate.
- Add-to-cart rate.
- Average order value.
- Repeat purchase rate.
- Checkout completion.

### Creative

- Reach.
- Engagement rate.
- Share/save rate.
- Video completion rate.
- Creative quality score.
- Brand recall proxy/measurement where available.

### Operations

- Stockout rate.
- Waste.
- Production yield.
- Order fulfilment SLA.
- Refund/cancellation rate.

### AI

- Generation success rate.
- QA rejection rate.
- Average generations per approved asset.
- Provider latency.
- Fallback rate.
- Cost per approved asset where measurable.

## 12. Acceptance Criteria

The integrated MVP is complete only when:

- [ ] Customer can browse products.
- [ ] Customer can add products to DOH Box.
- [ ] Customer can complete checkout through configured payment infrastructure.
- [ ] Orders are persisted and visible to operations.
- [ ] Product availability can prevent overselling.
- [ ] A brief can become a valid Creative Genome.
- [ ] Prompts can be compiled through the prompt contract.
- [ ] Provider failures produce controlled fallback behaviour.
- [ ] Generated assets can be QA-approved/rejected.
- [ ] Approved assets receive stable IDs and provenance.
- [ ] Analytics capture critical ecommerce and creative events.
- [ ] Cross-document links remain valid.

## 13. Delivery Phases

### Phase 0 — Foundation

- Canonical documentation.
- Brand truth.
- Design system.
- Schemas.
- Governance.

### Phase 1 — Ecommerce MVP

- Catalogue.
- Product pages.
- DOH Box.
- Checkout.
- Orders.
- Customer basics.

### Phase 2 — Creative Studio

- Brief Builder.
- Creative Genome.
- Prompt Compiler.
- Generation adapters.
- QA.
- Asset Registry.

### Phase 3 — ERP Foundations

- Inventory.
- Production.
- Procurement.
- Fulfilment.
- Reconciliation.

### Phase 4 — Intelligence

- Creative Memory.
- Performance feedback.
- Routing optimisation.
- Automated QA.
- Recommendation systems.

## 14. Risks

- Brand drift from uncontrolled AI output.
- IP risk from parody/presentation.
- Inventory race conditions.
- Payment/delivery provider failures.
- Incorrect business facts in AI-generated copy.
- PII leakage.
- Excessive coupling to one AI provider.
- Poor observability causing silent creative failures.

## 15. Definition of Done

A feature is not complete until its requirement, UX, architecture boundary, data contract, security/privacy impact, QA criteria, implementation, documentation and version history are aligned.
