---
title: "DOHNUT AI Provider Architecture"
date: "2026-08-31"
version: "1.0.0"
author: "GangNiaga Sdn. Bhd. / DOHNUT"
status: "approved"
tags: [ai, providers, routing, fallback, orchestration]
related_documents:
  - "./prompt-system-v1.0.0.md"
  - "../visual-ai/visual-ai-engine-v1.0.0.md"
  - "../schemas/asset-registry-v1.0.0.md"
  - "../governance/quality-gates-v1.0.0.md"
---

# DOHNUT AI Provider Architecture

## 1. Design principle

**Brand logic is provider-agnostic. Provider syntax is adapter-specific.**

## 2. Architecture

```text
CREATIVE GENOME
      ↓
PROMPT CORE
      ↓
PROVIDER ADAPTER
 ┌────┼───────┬───────┐
 ↓    ↓       ↓       ↓
Image Video   Copy   Other
Provider A ...
```

## 3. Routing policy

1. Select the best available provider for the task.
2. Validate capability and constraints before execution.
3. Retry transient failures within a bounded limit.
4. Fall back to the next compatible provider when health or capability checks fail.
5. Escalate to human review when all compatible routes fail or when quality cannot be guaranteed.

## 4. Provider adapter contract

```yaml
provider_id: provider-example
capabilities:
  - image
  - video
input_format: text+structured-brief
output_format: asset
supports_reference_image: true
supports_negative_prompt: false
health_endpoint: optional
fallback_priority: 2
```

## 5. Google Flow

Google Flow remains a supported visual execution target, but it is not the definition of the entire Visual AI Engine. Provider-specific instructions belong in the Google Flow template.
