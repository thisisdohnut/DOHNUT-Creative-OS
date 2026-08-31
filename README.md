# 🍩 DOHNUT Commerce + Creative OS

> **GOOD VIBE. GOOD DOH.**

![DOHNUT Creative OS system overview](assets/dohnut-creative-os-system-overview.svg)

DOHNUT Commerce + Creative OS ialah blueprint produk bersepadu untuk membina **D2C ecommerce + Creative Studio + AI Creative Engine + Operations/ERP** bagi DOHNUT, Malaysian-born premium donut D2C brand di bawah **GangNiaga Sdn. Bhd.**

## Canonical Project Model

```text
DOHNUT-Creative-OS
      │
      │ canonical creative intelligence
      ▼
Creative OS
      │
      ├── Brand Truth
      ├── DOH Language™
      ├── DOH Cinema™ / DOHFLIX™
      ├── Doh Boy™
      ├── Pop Culture Playbook™
      ├── Creative Genome
      ├── Visual Benchmark
      ├── Prompt System
      ├── Quality / Governance
      └── Creative Memory

      │ integration contract
      ▼
thisidowgnut-source/Dowgnut-Custom
      │
      ├── Storefront
      ├── Product Catalogue
      ├── DOH Box / Cart
      ├── Checkout
      ├── Customer Account
      ├── Orders
      └── Application Runtime
```

> [!IMPORTANT]
> **DOHNUT-Creative-OS** ialah canonical creative/intelligence layer. **Dowgnut-Custom** ialah ecommerce/application layer. Integrasi dibuat melalui versioned contracts, bukan dengan menyalin semua documentation ke dalam application repository.

## Master Development Documents

| File | Fungsi | Source of truth |
| --- | --- | --- |
| [PRD.md](PRD.md) | What to build, users, requirements, acceptance criteria | Product requirements |
| [ARCHITECTURE.md](ARCHITECTURE.md) | System boundaries, services, data, events, integration | Technical architecture |
| [DESIGN.md](DESIGN.md) | UI/UX, Figma, visual system, components, flows | Experience/design |
| [ERP.md](ERP.md) | Inventory, production, procurement, fulfilment, finance | Operations |
| [PROMPT.md](PROMPT.md) | Prompt contracts, Creative Genome, routing, provider adapters | AI execution |

## Existing Creative Documentation

| Module | Document |
| --- | --- |
| Brand Constitution | [Brand Constitution](docs/brand/brand-constitution-v1.0.0.md) |
| DOH Language™ | [DOH Language](docs/creative/doh-language-v1.0.0.md) |
| DOH Cinema™ | [DOH Cinema](docs/creative/doh-cinema-v1.0.0.md) |
| Doh Boy™ | [Doh Boy](docs/creative/doh-boy-v1.0.0.md) |
| Pop Culture Playbook™ | [Playbook](docs/creative/pop-culture-playbook-v1.0.0.md) |
| Visual AI Engine™ | [Visual AI Engine](docs/visual-ai/visual-ai-engine-v1.0.0.md) |
| Creative Genome | [Creative Genome](docs/visual-ai/creative-genome-v1.0.0.md) |
| Visual Benchmark | [Visual Benchmark](docs/visual-ai/dohnut-visual-benchmark-v1.0.0.md) |
| Governance | [Governance](docs/governance/governance-v1.0.0.md) |
| Quality Gates | [Quality Gates](docs/governance/quality-gates-v1.0.0.md) |

## Product Vision

DOHNUT bukan sekadar ecommerce dan bukan sekadar prompt generator. Ia ialah satu **brand-aware commerce system** yang menyambungkan creative intelligence kepada customer experience dan business operations.

```text
Brand Truth
    ↓
Creative Intelligence
    ↓
Content / Campaign
    ↓
Ecommerce
    ↓
Order
    ↓
Operations / ERP
    ↓
Customer
    ↓
Performance
    ↓
Creative Memory
    ↺
```

## Visual North Star

DOHNUT menggunakan **premium commercial food photography** sebagai asas. Tactile dan playful diterjemahkan melalui materiality, softness, rounded forms, bold colour dan controlled exaggeration — bukan menjadikan setiap visual seperti plastic CGI.

> **REAL FOOD FIRST. PLAY SECOND. BRAND ALWAYS.**

### Three-question visual test

1. **Can I Taste It?** — appetizing, fresh, edible.
2. **Can I Feel It?** — tactile, soft, dimensional.
3. **Can I Recognize It?** — distinctive enough to feel like DOHNUT without depending only on the logo.

## Customer Journey

```text
LANDING
  ↓
SHOP
  ↓
PRODUCT
  ↓
ADD TO DOH BOX
  ↓
CART
  ↓
CHECKOUT
  ↓
PAYMENT
  ↓
ORDER CONFIRMED
  ↓
FULFILMENT
  ↓
DELIVERY / PICKUP
  ↓
REORDER
```

## Creative Studio Journey

```text
BRIEF
  ↓
CREATIVE GENOME
  ↓
MODULE ROUTING
  ↓
PROMPT COMPILATION
  ↓
PROVIDER ADAPTER
  ↓
GENERATION
  ↓
QUALITY GATES
  ↓
APPROVAL
  ↓
ASSET REGISTRY
  ↓
PUBLICATION
  ↓
PERFORMANCE
  ↓
CREATIVE MEMORY
```

## ERP Journey

```text
DEMAND / ORDER
  ↓
INVENTORY
  ↓
PRODUCTION
  ↓
PROCUREMENT
  ↓
FULFILMENT
  ↓
RECONCILIATION
  ↓
REPORTING
```

## Development Sequence

### Phase 0 — Foundation

- Read the [PRD](PRD.md).
- Lock the architecture in [ARCHITECTURE](ARCHITECTURE.md).
- Implement design system and user flows from [DESIGN](DESIGN.md).
- Establish ERP boundaries using [ERP](ERP.md).
- Establish prompt contracts using [PROMPT](PROMPT.md).

### Phase 1 — Ecommerce MVP

- Product catalogue.
- Product detail.
- DOH Box/cart.
- Checkout.
- Orders.
- Customer basics.

### Phase 2 — Creative Studio

- Brief Builder.
- Creative Genome.
- DOH modules.
- Prompt Builder.
- Generation adapters.
- QA.
- Asset Registry.

### Phase 3 — Operations / ERP

- Inventory.
- Production.
- Procurement.
- Fulfilment.
- Reconciliation.
- Reporting.

### Phase 4 — Intelligence

- Creative Memory.
- Performance feedback.
- Automated QA.
- Model/provider routing.
- Recommendation and optimisation.

## Quality Gate

Sebelum release:

- [ ] Requirement mapped to PRD.
- [ ] UX represented in Figma.
- [ ] Architecture boundary documented.
- [ ] Data contract exists where needed.
- [ ] Security/privacy reviewed.
- [ ] QA criteria exist.
- [ ] Asset provenance is retained.
- [ ] Cross-links resolve.
- [ ] Version and changelog updated.
- [ ] Critical runtime tests pass.

## Governance

Lower-level creative output tidak boleh override higher-level brand, legal, operational atau financial truth.

> [!WARNING]
> Jangan gunakan parody untuk mendakwa endorsement. Jangan copy protected logos, artwork, characters atau exact poster compositions. Jangan letakkan secrets atau sensitive customer data dalam prompts.

## Contributing

Rujuk [CONTRIBUTING.md](CONTRIBUTING.md). Semua perubahan besar perlu menyatakan scope, owner, version impact dan quality checks.

## Related Application Repository

[Ecommerce Application — Dowgnut-Custom](https://github.com/thisidowgnut-source/Dowgnut-Custom)

## Version

Documentation baseline: **v1.0.0**.

Lihat [CHANGELOG](docs/governance/changelog.md) dan [System Index](docs/00-system-index.md) untuk governance dan system map.
