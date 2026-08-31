---
title: "DOHNUT Visual Benchmark"
date: "2026-08-31"
version: "1.0.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "draf"
tags: [visual-ai, benchmark, product-photography, brand-consistency]
related_documents:
  - "./visual-ai-engine-v1.0.0.md"
  - "./creative-genome-v1.0.0.md"
  - "./google-flow-prompt-template-v1.0.0.md"
  - "../brand/brand-constitution-v1.0.0.md"
---

# DOHNUT Visual Benchmark

## 1. Benchmark status

**Status: MASTER VISUAL REFERENCE**

This document establishes the original user-provided chocolate-hazelnut stuffed donut image as the **North Star benchmark** for DOHNUT product hero imagery.

The benchmark is a visual quality reference, not an instruction to reproduce the exact composition in every asset.

## 2. Source asset

- Source filename: `Chocolate-hazelnut_filling_oozin…_2K_202608312008.jpeg`
- Local source hash (SHA-256): `1adc7b8196ad3284627eb21b0c4a403f6c54a4b018a1ee7e5cfab2ee6e843008`
- Role: reference benchmark for product hero generation

## 3. Visual north star

The benchmark succeeds because it balances **real food appetitiveness**, **premium commercial photography**, **controlled tactile quality**, **bold DOHNUT yellow**, and **brand presence** without becoming overly CGI or cartoon-like.

## 4. Benchmark characteristics

| Dimension | Benchmark standard |
| --- | --- |
| Product realism | High; recognizably baked food |
| Dough | Thick, soft, fluffy, golden-brown, natural texture |
| Filling | Glossy chocolate-hazelnut; visibly indulgent but believable |
| Filling behaviour | Natural overflow/ooze with realistic gravity and viscosity |
| Composition | Single hero product; balanced scale; generous breathing room |
| Background | Clean, bold yellow; minimal distraction |
| Lighting | Soft studio light; gentle highlights; controlled contact shadow |
| Tactility | Soft and edible; never plastic-looking |
| Brand presence | Official logo clearly visible, preferably composited from approved artwork |
| Overall tone | Premium + playful + appetizing |

## 5. Three-question test

### Can I Taste It?

The viewer should immediately perceive freshness, softness, filling richness and indulgence.

### Can I Feel It?

The dough, filling and toppings should communicate physical materiality without looking synthetic.

### Can I Recognize It?

With the logo present, the asset must read as DOHNUT. Without the logo, it should still retain at least several DOHNUT visual signals: bold colour, tactile food styling, rounded product language and playful premium composition.

## 6. Priority hierarchy

When generation quality conflicts, use this order:

1. Product appetitiveness and food realism.
2. Dough and filling texture.
3. Composition and lighting.
4. DOHNUT colour environment.
5. Brand asset placement.
6. Experimental/playful embellishment.

Playfulness must never damage food realism.

## 7. Logo handling rule

**Do not rely on an image model to redraw the master DOHNUT logo.**

Preferred pipeline:

```text
AI generates clean product visual
        ↓
Approved DOHNUT logo asset
        ↓
Figma / design composition
        ↓
Final branded artwork
```

## 8. What to avoid

- Oversized CGI-looking donut that dominates the frame.
- Plastic or toy-like dough.
- Excessive filling that looks physically impossible.
- Overly glossy surfaces that feel synthetic.
- Busy props or decorative clutter.
- Generic luxury-food styling that removes DOHNUT personality.
- Cartoonization of the food hero.
- AI-generated or distorted brand logo.

## 9. Benchmark scorecard

A candidate hero image should be scored from 1–10.

| Score | Requirement |
| --- | --- |
| 9–10 | Master-reference quality; suitable for campaign foundation |
| 8–8.9 | Strong; minor refinement only |
| 7–7.9 | Usable but requires creative revision |
| 6–6.9 | Significant mismatch; regenerate |
| <6 | Reject |

Minimum recommended pass thresholds:

- Food realism: **9**
- Tactility: **8**
- Composition: **8**
- Brand recognizability: **8**
- Overall DOHNUT feel: **8.5**

## 10. Relationship to the Visual AI Engine

All new product hero prompts should reference this benchmark before generation. The benchmark overrides generic style defaults when they conflict with the approved DOHNUT visual direction.

## 11. Benchmark principle

> **REAL FOOD FIRST. PLAY SECOND. BRAND ALWAYS.**

This is the operating rule for future DOHNUT visual generation.
