---
title: "DOHNUT Visual AI Engine™"
date: "2026-08-31"
version: "1.0.1"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "draf"
tags: [visual-ai, prompt-engineering, google-flow, image-generation, video-generation, benchmark]
related_documents:
  - "../brand/brand-constitution-v1.0.0.md"
  - "../creative/doh-language-v1.0.0.md"
  - "../creative/doh-cinema-v1.0.0.md"
  - "../creative/doh-boy-v1.0.0.md"
  - "../creative/pop-culture-playbook-v1.0.0.md"
  - "./creative-genome-v1.0.0.md"
  - "./dohnut-visual-benchmark-v1.0.0.md"
  - "../ai/prompt-system-v1.0.0.md"
---

# DOHNUT Visual AI Engine™

## 1. Objective

Sistem generatif modular yang menukar **brand truth + product + culture + creative concept** menjadi prompt yang konsisten untuk Google Flow dan model generatif lain.

## 2. Architecture

```text
BRAND TRUTH
  ↓
VISUAL BENCHMARK
  ↓
CREATIVE GENOME
  ↓
DOH LANGUAGE ── DOH CINEMA ── DOH BOY
  ↓
POP CULTURE ADAPTER
  ↓
PROMPT COMPILER
  ↓
GOOGLE FLOW / IMAGE / VIDEO MODEL
  ↓
VISUAL QA
  ↓
ASSET REGISTRY
  ↓
PERFORMANCE FEEDBACK
  ↓
CREATIVE MEMORY
```

## 3. Master visual benchmark

The original user-provided chocolate-hazelnut stuffed donut image is the **MASTER VISUAL REFERENCE / NORTH STAR** for DOHNUT product hero imagery.

See [DOHNUT Visual Benchmark](./dohnut-visual-benchmark-v1.0.0.md).

### Benchmark rule

> **REAL FOOD FIRST. PLAY SECOND. BRAND ALWAYS.**

Generic AI style presets must not override benchmark characteristics when they conflict with the approved visual direction.

## 4. Visual promise

### Can I Taste It?
Food texture, scale, filling, freshness dan lighting mesti nampak appetizing.

### Can I Feel It?
Bentuk lembut, tactile, rounded dan material quality mesti terasa secara visual.

### Can I Recognize It?
Walaupun logo dikeluarkan, visual mesti masih terasa seperti DOHNUT.

## 5. Prompt tiers

| Tier | Purpose |
| --- | --- |
| T1 | Product hero |
| T2 | Brand visual |
| T3 | Campaign scene |
| T4 | Pop culture / DOH Cinema |
| T5 | Hero integrated campaign |

## 6. Variable system

`product_type`, `flavour`, `filling_behaviour`, `camera`, `lighting`, `background`, `environment`, `character_mode`, `cinema_mode`, `copy`, `platform`, `objective`, `benchmark_mode`.

## 7. Master visual instruction

```text
Create a premium hero visual for DOHNUT, a Malaysian-born premium donut D2C brand.

BENCHMARK
Use the DOHNUT Visual Benchmark as the primary quality reference.
Preserve the benchmark's balance of realistic baked food, soft tactile dough,
credible filling behaviour, premium commercial lighting, bold clean yellow,
and restrained playful energy.

SUBJECT
A premium [DONUT TYPE / FLAVOUR] donut with [PRODUCT CHARACTERISTICS].

PRODUCT FORM
Thick, soft, rounded, perfectly baked dough with realistic food texture and tactile, slightly squishy visual quality.

FILLING / TOPPING
[INSERT FILLING OR TOPPING]. Show realistic viscosity, gloss, texture and natural movement.

VISUAL LANGUAGE
Premium commercial food photography combined with controlled tactile materiality,
playful rounded forms and bold contemporary branding. Avoid overly synthetic CGI.

LIGHTING
Soft professional studio lighting, gentle highlights and controlled contact shadows.

COMPOSITION
Hero product dominance, balanced scale, clean composition and generous negative space.

BACKGROUND
Use the approved DOHNUT yellow or another approved campaign background.

BRAND DNA
Playful. Bold. Tactile. Premium. Authentic. Youthful. Internet-native.

LOGO
Do not redraw the master DOHNUT logo with the model. Leave clean space for approved artwork to be composited later.

AVOID
Generic bakery photography, plastic food, over-exaggerated CGI, distorted branding,
unrelated colours, copied protected assets, clutter and unexplained text.
```

## 8. Example — Chocolate Hazelnut

> A premium stuffed chocolate-hazelnut donut matching the DOHNUT Visual Benchmark: thick golden-brown soft dough, believable baked texture, rich glossy filling overflowing naturally from the center, clean saturated yellow background, soft studio lighting, balanced premium composition and restrained tactile playfulness.

## 9. Example — DOH WICK campaign

> A cinematic DOHNUT action campaign featuring a chocolate-hazelnut stuffed donut as the hero. Use the benchmark for food realism, dough texture, colour discipline and premium product rendering. Add original action-film visual language, dramatic but controlled lighting, Doh Boy in action-hero mode, rich filling visible, bold DOHNUT yellow environment, original typography and composition. Headline: DOH WICK. Subheadline: THE LAST BITE. Keep the execution original and do not reproduce any protected movie poster or character asset.

## 10. Benchmark QA override

When a candidate image looks more artificial, more cluttered, more exaggerated or less appetizing than the benchmark, **regenerate** rather than adding more decorative effects.
