---
title: "DOHNUT Structured AI Prompt System"
date: "2026-08-31"
version: "1.0.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "draf"
tags: [prompts, prompt-engineering, few-shot, ai]
related_documents:
  - "../brand/brand-constitution-v1.0.0.md"
  - "../visual-ai/creative-genome-v1.0.0.md"
  - "../schemas/data-contracts-v1.0.0.md"
  - "../governance/quality-gates-v1.0.0.md"
---

# DOHNUT Structured AI Prompt System

## 1. Standard prompt contract

Setiap prompt mesti mempunyai:

1. `context`
2. `persona`
3. `required_inputs`
4. `optional_inputs`
5. `output_format`
6. `constraints`
7. `few_shot_examples` untuk task kompleks
8. `self_check`
9. `version`

## 2. Prompt modules

| ID | Modul | Persona | Output |
| --- | --- | --- | --- |
| PRM-01 | Brand Strategy | senior brand strategist | positioning + recommendations |
| PRM-02 | Content | creative copywriter | copy pack |
| PRM-03 | Pop Culture | cultural creative director | parody concepts |
| PRM-04 | Social | social strategist | hooks + calendar |
| PRM-05 | Packaging | packaging copy lead | hierarchy + copy |
| PRM-06 | Campaign | integrated creative director | campaign system |
| PRM-07 | Visual Direction | art director | visual brief/prompt |
| PRM-08 | Data Analysis | D2C analyst | insights |
| PRM-09 | QA | brand QA reviewer | score + findings |
| PRM-10 | Project | creative producer | plan + risks |
| PRM-11 | Orchestration | AI router | prompt/skill chain |
| PRM-12 | Documentation | documentation maintainer | synchronized docs |

## 3. Master prompt template

```text
CONTEXT
You are operating inside DOHNUT Creative OS...

ROLE
Act as [persona].

INPUTS
Required: [fields]
Optional: [fields]

TASK
[explicit task]

BRAND RULES
Use Brand Constitution and controlled glossary.

OUTPUT
Return:
1. summary
2. deliverables
3. assumptions
4. risks
5. qa_status
6. version

CONSTRAINTS
Do not invent missing critical data. Escalate legal, safety, privacy or regulatory issues.

FEW-SHOT EXAMPLES
[2-3 examples]

SELF-CHECK
Verify brand consistency, factual support, structure, safety and requested format.
```

## 4. Few-shot standard

### Example — DOH copy

Input: Product launch for chocolate-hazelnut stuffed donut.

Good output:

> **DOH NUT WAIT.**
> Chocolate Hazelnut just dropped.

Why: recognisable pun + direct product relevance + short.

### Example — Visual prompt

Input: Premium stuffed donut, tactile style, yellow background.

Good output: preserve product specificity, lighting, texture, brand palette and avoid generic bakery language.

## 5. Routing rule

Gunakan satu prompt untuk satu deliverable. Gunakan **PRM-11 Orchestration** apabila satu request memerlukan dua atau lebih prompt families.
