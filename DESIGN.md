---
title: "DOHNUT Commerce + Creative OS — Design System"
date: "2026-08-31"
version: "1.0.0"
author: "DOHNUT / GangNiaga Sdn. Bhd."
status: "draf"
tags: [design, figma, ux, ui, ecommerce, creative-studio]
related_documents: ["./README.md", "./PRD.md", "./ARCHITECTURE.md", "./ERP.md", "./PROMPT.md"]
---

# DOHNUT Commerce + Creative OS — Design System

## 1. Design Vision

Design system ini menyatukan ecommerce dan Creative Studio di bawah satu bahasa visual DOHNUT.

> **REAL FOOD FIRST. PLAY SECOND. BRAND ALWAYS.**

DOHNUT perlu kelihatan **premium, tactile, playful dan moden**, bukan generic bakery site dan bukan plastic CGI brand.

## 2. Visual North Star

### Product

- Thick, soft, fluffy baked dough.
- Believable filling and topping behaviour.
- Premium commercial food photography.
- Controlled tactile materiality.
- High appetite appeal.

### Brand

- Bold colour blocks.
- Rounded geometry.
- Confident typography.
- Generous negative space.
- Playful microcopy.

## 3. Colour Tokens

Gunakan design tokens sebagai single source untuk UI. Nilai akhir hendaklah datang daripada approved brand source, bukan copy-paste manual.

| Token | Usage |
| --- | --- |
| `brand.navy` | Primary text, dark surfaces, primary CTA |
| `brand.pink` | Playful accent |
| `brand.lime` | High-energy action/accent |
| `brand.yellow` | Hero/campaign background |
| `brand.cream` | Warm neutral/background |

## 4. Typography

Typography mesti menyokong:
- high-impact headlines.
- short campaign copy.
- readable product information.
- clear price hierarchy.
- accessible UI text.

Setiap typography change mesti dikemas kini dalam canonical brand documentation dan design tokens.

## 5. Layout System

Recommended spacing scale:

```text
4 / 8 / 12 / 16 / 24 / 32 / 48 / 64 / 96 / 128
```

Gunakan 12-column desktop grid dan responsive mobile grid dengan content max-width yang konsisten.

## 6. UI Principles

### Product First

Product imagery sentiasa menjadi primary visual hierarchy pada ecommerce.

### Playful, Not Chaotic

Gunakan:
- rounded forms.
- bold blocks.
- controlled asymmetry.
- concise jokes.

Elakkan:
- visual clutter.
- excessive drop shadows.
- novelty typography yang mengurangkan readability.
- generic AI-art aesthetic.

### Conversion Clarity

CTA utama mesti jelas:

- **SHOP THE DOH**
- **ADD TO DOH BOX**
- **CHECKOUT**
- **REORDER THE DOH**

## 7. Ecommerce Screens

### 7.1 Landing Page

```text
Announcement
→ Header
→ Hero
→ Signature Drop
→ Product Discovery
→ Brand Story
→ DOH Cinema / Campaign
→ Social Proof
→ CTA
→ Footer
```

### 7.2 Shop

- Search.
- Category filter.
- Product grid.
- Availability.
- Price.
- Add to DOH Box.

### 7.3 Product Detail

- Hero.
- Gallery.
- Product facts.
- Price.
- Quantity.
- CTA.
- Delivery/pickup.
- Related items.

### 7.4 DOH Box

- Cart items.
- Quantity.
- Promo.
- Delivery/pickup.
- Subtotal.
- Checkout CTA.

### 7.5 Checkout

- Customer details.
- Delivery.
- Payment.
- Order review.
- Confirmation.

## 8. Creative Studio Screens

```text
Dashboard
→ New Brief
→ Creative Genome
→ Module Selection
→ Prompt Builder
→ Generate
→ QA
→ Asset
→ Campaign
```

### Creative OS modules

- Brand Truth.
- DOH Language™.
- DOH Cinema™.
- Doh Boy™.
- Pop Culture Playbook™.
- Visual AI Engine™.
- Asset Registry.
- Creative Memory.

## 9. Component Inventory

Minimum shared component library:

- Header.
- Nav.
- Button.
- ProductCard.
- ProductGallery.
- Price.
- QuantitySelector.
- CartItem.
- CheckoutSummary.
- Badge.
- CampaignCard.
- DohPunCard.
- CreativeModuleCard.
- PromptEditor.
- GenerationResult.
- QAStatus.
- AssetCard.
- ApprovalPanel.
- DataTable.
- Modal.
- Toast.
- EmptyState.
- ErrorState.
- LoadingState.

## 10. Responsive Design

Support minimum:
- mobile.
- tablet.
- desktop.

Primary ecommerce actions must remain visible and usable on mobile without hover-only interaction.

## 11. Accessibility

- Keyboard navigable.
- Visible focus state.
- Semantic labels.
- Image alt text.
- Sufficient contrast.
- Reduced-motion preference.
- Clear form errors.
- Never rely on colour alone.

## 12. Figma Organisation

Recommended pages:

```text
00 — Cover
01 — Foundations
02 — Components
03 — Ecommerce
04 — Creative Studio
05 — Campaigns
06 — Prototypes
07 — QA / Handoff
```

## 13. Asset Handling

Official logos and approved product images are source assets. AI generation must not redraw official logos. The AI output is composed with approved brand assets during design assembly.

## 14. Design QA

- [ ] Correct tokens.
- [ ] Correct logo.
- [ ] Correct visual benchmark.
- [ ] Mobile/desktop states.
- [ ] Loading/error/empty states.
- [ ] Accessibility checks.
- [ ] DOH Language™ copy check.
- [ ] Consistent component variants.
- [ ] Developer handoff notes.
