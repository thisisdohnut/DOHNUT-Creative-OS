---
title: "DOHNUT Commerce + ERP — Enterprise Resource Planning Specification"
date: "2026-08-31"
version: "1.0.0"
author: "DOHNUT / GangNiaga Sdn. Bhd."
status: "draf"
tags: [erp, inventory, production, procurement, fulfilment, finance, ecommerce]
related_documents: ["./README.md", "./PRD.md", "./ARCHITECTURE.md", "./DESIGN.md", "./PROMPT.md"]
---

# DOHNUT Commerce + ERP — Enterprise Resource Planning Specification

## 1. Purpose

ERP ialah operations backbone untuk menyambungkan ecommerce kepada inventory, production, procurement, fulfilment dan finance. ERP kekal authoritative untuk operational and financial truth.

Creative OS tidak boleh mengubah financial truth, inventory truth atau order truth secara arbitrari.

## 2. Boundary

```text
CREATIVE OS
Brand / Campaign / Prompt / Asset
          │
          ▼
COMMERCE
Product / Cart / Order / Customer
          │
          ▼
ERP
Inventory / Production / Procurement / Fulfilment / Finance
```

## 3. ERP Modules

| Module | Responsibility |
| --- | --- |
| Product Master | SKU, variants, pricing metadata |
| Inventory | Stock, reservations, movements, locations |
| Production | Recipes, BOM, batches, yield |
| Procurement | Suppliers, POs, receiving |
| Sales | Orders and channel attribution |
| Fulfilment | Packing, dispatch, delivery/pickup |
| Customer | Operational customer records |
| Finance | Payment, refund, reconciliation |
| Reporting | Operational and financial reporting |

## 4. Product Master

Minimum contract:

```yaml
product_id:
sku:
name:
category:
variant:
price:
cost:
status:
availability:
tax_class:
inventory_tracking:
recipe_id:
creative_asset_id:
```

Only designated commerce/finance roles may mutate authoritative price or tax fields.

## 5. Inventory Model

Track at minimum:

- on_hand
- reserved
- available
- unavailable
- damaged
- expired
- in_production

```text
available = on_hand - reserved - unavailable
```

Every adjustment needs a reason code and audit record.

## 6. Recipe and BOM

```text
Finished Product
├── Dough
├── Filling
├── Topping
├── Packaging
└── Insert / Label
```

Recipe/BOM revisions require version control because they affect cost and production planning.

## 7. Production Flow

```text
Demand
→ Production Plan
→ Material Reservation
→ Batch
→ Food/Quality Check
→ Finished Stock
→ Available for Sale
```

Production data should support planned-vs-actual yield and waste analysis.

## 8. Procurement Flow

```text
Reorder Signal
→ Purchase Request
→ Approval
→ Purchase Order
→ Supplier
→ Receiving
→ Inventory Update
→ Reconciliation
```

Supplier master should retain lead time, active status, pricing history and relevant terms.

## 9. Order Lifecycle

```text
DRAFT
→ PENDING_PAYMENT
→ PAID
→ ACCEPTED
→ PREPARING
→ READY
→ DISPATCHED
→ DELIVERED
```

Terminal/exception states may include:

```text
CANCELLED
REFUNDED
FAILED
```

Transitions must be validated and audited.

## 10. Payments

Never store raw card/payment credentials in DOHNUT application databases unless a specific compliant architecture requires otherwise.

Store only what is operationally needed:
- provider
- transaction reference
- amount
- currency
- status
- timestamps
- reconciliation status

## 11. Fulfilment

```text
Paid Order
→ Allocate Stock
→ Pick
→ Pack
→ Handoff
→ Delivery / Pickup
→ Complete
```

Track fulfilment IDs separately from order IDs so retries and exceptions remain auditable.

## 12. Customer Data

- Minimise PII.
- Restrict access by role.
- Separate marketing consent from order necessity.
- Define retention rules.
- Do not expose sensitive customer information to creative generation prompts.

## 13. Reporting

### Sales

- gross sales
- net sales
- orders
- average order value
- units per order

### Inventory

- stockout rate
- inventory accuracy
- waste
- turnover

### Production

- yield
- waste
- planned-vs-actual
- batch exceptions

### Procurement

- supplier lead time
- price variance
- fulfilment rate

### Customer

- repeat rate
- reorder interval
- retention

## 14. Creative OS Integration

ERP may expose facts to Creative OS only when marked canonical:

- product name
- product ID
- approved price
- approved availability
- campaign eligibility
- operational constraints

Creative OS may return:
- approved asset IDs
- campaign IDs
- creative metadata
- approved copy variants

Creative AI must never invent price, inventory, ingredient or fulfilment claims.

## 15. Idempotency and Audit

Critical operations must be idempotent where retries are possible:

- payment confirmation
- order creation
- inventory reservation
- refund
- fulfilment completion

Maintain audit records for:
- price changes
- inventory adjustments
- refunds
- status overrides
- permission changes

## 16. ERP MVP Priority

1. Product Master.
2. Orders.
3. Inventory.
4. Fulfilment.
5. Payments/reconciliation.
6. Procurement.
7. Production.
8. Reporting.

## 17. ERP Definition of Done

- [ ] Product master is authoritative.
- [ ] SKU is unique.
- [ ] Prices are controlled.
- [ ] Inventory movements are auditable.
- [ ] Orders have validated state transitions.
- [ ] Payment references are secure.
- [ ] Refunds are permission-controlled.
- [ ] Ecommerce availability sync is defined.
- [ ] Production and BOM revisions are versioned.
- [ ] Reporting metrics have documented definitions.
