# Contributing to DOHNUT Creative OS

Terima kasih kerana menyumbang kepada **DOHNUT Creative OS**.

## Contribution flow

```text
IDEA
  ↓
CLASSIFY
  ↓
CHECK SOURCE OF TRUTH
  ↓
CREATE / UPDATE DOCUMENT
  ↓
RUN QUALITY GATES
  ↓
UPDATE VERSION + CROSS-REFERENCES
  ↓
UPDATE CHANGELOG
  ↓
PUBLISH
```

## Before submitting

- Nyatakan objective dan scope.
- Kenal pasti module berkaitan.
- Semak [Source of Truth hierarchy](docs/governance/source-of-truth-hierarchy-v1.0.0.md).
- Gunakan [Markdown authoring standard](docs/governance/markdown-authoring-standard-v1.0.0.md).
- Jalankan [Quality Gates](docs/governance/quality-gates-v1.0.0.md).
- Tentukan semantic version impact.

## New ideas

Idea yang belum diluluskan mesti ditanda `draft` atau `experimental` dan tidak boleh dipersembahkan sebagai official Brand Truth.

## Campaign naming

Gunakan format:

```text
campaign-slug-v1.0.0.md
```

Untuk asset runtime, simpan `campaign_id` dan `version` dalam Asset Registry.

## Do not commit

- Secrets, API keys, passwords atau customer PII.
- Unlicensed protected assets.
- AI-generated logos yang belum diluluskan sebagai official brand assets.
- Regulatory or food-safety claims tanpa human review.
