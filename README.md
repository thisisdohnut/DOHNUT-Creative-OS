# DOHNUT Creative OS

> **GOOD VIBE. GOOD DOH.**

![DOHNUT Creative OS system overview](assets/dohnut-creative-os-system-overview.svg)

**DOHNUT Creative OS** ialah sistem operasi kreatif dan dokumentasi AI untuk **DOHNUT**, sebuah Malaysian-born premium donut D2C brand di bawah **GangNiaga Sdn. Bhd.**, berfokus di KL/Selangor (Lembah Klang), dengan model online-first dan delivery-led.

> [!IMPORTANT]
> Repository ini ialah **canonical source** untuk Brand Truth, creative modules, AI prompt contracts, visual generation standards, governance dan creative memory.

## Apa itu DOHNUT Creative OS?

DOHNUT Creative OS menukar **brand truth + structured brief + creative language + culture + AI tooling** kepada output kreatif yang boleh dihasilkan secara konsisten, diuji, diluluskan dan dipelajari semula.

### Core stack

```text
BRAND TRUTH
    ↓
CONTROLLED GLOSSARY
    ↓
CREATIVE GENOME
    ↓
DOH LANGUAGE™ ── DOH CINEMA™ ── DOH BOY™
    ↓
POP CULTURE ADAPTER
    ↓
PROMPT COMPILER
    ↓
IMAGE / VIDEO / CONTENT GENERATION
    ↓
QUALITY GATES
    ↓
ASSET REGISTRY
    ↓
PERFORMANCE + CREATIVE MEMORY
```

## Brand Core

| Field | Standard |
| --- | --- |
| **Brand** | DOHNUT / Doh-Nut |
| **Company** | GangNiaga Sdn. Bhd. |
| **Market** | Malaysia |
| **Primary geography** | KL / Selangor / Klang Valley |
| **Business model** | D2C, online-first, delivery-led |
| **Product** | Premium donuts: classic, sprinkled, stuffed, specialty, signature |
| **Tagline** | **GOOD VIBE. GOOD DOH.** |
| **Creative DNA** | Playful, bold, tactile, premium, authentic |
| **Verbal universe** | **DOH Language™** |
| **Story universe** | **DOH Cinema™ / DOHFLIX™** |
| **Character universe** | **Doh Boy™** |

## Visual North Star

DOHNUT menggunakan **premium commercial food photography** sebagai asas. Tactile dan playful diterjemahkan melalui materiality, softness, rounded forms, bold colour dan controlled exaggeration — bukan menjadikan setiap visual seperti plastic CGI.

**Visual benchmark:**

- Real food first.
- Soft, fluffy, believable dough.
- Indulgent but physically plausible filling.
- Clean, bold yellow background when the campaign token calls for it.
- Generous negative space.
- Premium lighting.
- Official brand assets are composited or referenced from approved sources; AI tidak boleh mereka semula logo secara arbitrari.

**Three-question test:**

1. **Can I Taste It?** — appetizing, fresh, edible.
2. **Can I Feel It?** — tactile, soft, dimensional.
3. **Can I Recognize It?** — distinctive enough to feel like DOHNUT without depending only on the logo.

## Creative Modules

| Module | Fungsi | Dokumen |
| --- | --- | --- |
| **Brand Constitution** | Source of truth | [Brand Constitution](docs/brand/brand-constitution-v1.0.0.md) |
| **DOH Language™** | Puns, hooks, verbal identity | [DOH Language](docs/creative/doh-language-v1.0.0.md) |
| **DOH Cinema™** | Parody, cinematic concepts, campaign stories | [DOH Cinema](docs/creative/doh-cinema-v1.0.0.md) |
| **Doh Boy™** | Character behaviour and voice | [Doh Boy](docs/creative/doh-boy-v1.0.0.md) |
| **Pop Culture Playbook™** | Culture-driven idea library | [Playbook](docs/creative/pop-culture-playbook-v1.0.0.md) |
| **Visual AI Engine™** | Prompt compilation and generation rules | [Visual AI Engine](docs/visual-ai/visual-ai-engine-v1.0.0.md) |
| **Creative Genome** | Machine-readable creative brief | [Creative Genome](docs/visual-ai/creative-genome-v1.0.0.md) |
| **AI Prompt System** | Structured task prompts | [Prompt System](docs/ai/prompt-system-v1.0.0.md) |
| **Governance** | Quality, safety, versioning | [Governance](docs/governance/governance-v1.0.0.md) |

## Visual Generation Workflow

```text
Brief
  ↓
Creative Genome
  ↓
Module Selection
  ↓
Prompt Compilation
  ↓
Provider Adapter
  ↓
Generation
  ↓
Visual QA
  ↓
Human Approval (when required)
  ↓
Asset Registry
  ↓
Performance Feedback
```

Provider-specific syntax is an implementation detail. Brand logic remains provider-agnostic.

## Quick Start

### 1. Mulakan dengan Brand Truth

Baca [System Index](docs/00-system-index.md) dan [Brand Constitution](docs/brand/brand-constitution-v1.0.0.md).

### 2. Tukar idea kepada Creative Genome

Contoh input minimum:

```json
{
  "objective": "product_launch",
  "product_type": "stuffed_donut",
  "flavour": "chocolate_hazelnut",
  "visual_tier": "T2",
  "camera": "three_quarter_front",
  "background": "dohnut_yellow",
  "character_mode": null,
  "cinema_mode": null
}
```

### 3. Pilih creative modules

Gunakan **DOH Language™** untuk copy, **DOH Cinema™** untuk narrative, **Doh Boy™** untuk character behaviour, dan **Pop Culture Playbook™** untuk cultural adaptation.

### 4. Compile prompt

Rujuk [Visual AI Engine](docs/visual-ai/visual-ai-engine-v1.0.0.md) dan [Google Flow Prompt Template](docs/visual-ai/google-flow-prompt-template-v1.0.0.md).

### 5. Run QA

Semak [Governance](docs/governance/governance-v1.0.0.md) dan [Quality Gates](docs/governance/quality-gates-v1.0.0.md).

## Documentation Standard

Semua machine-facing Markdown dalam `docs/` mesti menggunakan **YAML front matter**, semantic versioning dan cross-reference yang boleh dikesan. Untuk style dan struktur, rujuk [Markdown authoring standard](docs/governance/markdown-authoring-standard-v1.0.0.md).

## Repository Map

```text
.
├── README.md
├── assets/
│   └── dohnut-creative-os-system-overview.svg
├── docs/
│   ├── 00-system-index.md
│   ├── brand/
│   ├── creative/
│   ├── visual-ai/
│   ├── ai/
│   ├── schemas/
│   └── governance/
└── .github/
```

## Governance

DOHNUT Creative OS membezakan **approved truth**, **draft concepts** dan **experiments**. Lower-level creative output tidak boleh override higher-level brand or legal constraints.

> [!WARNING]
> Jangan gunakan parody sebagai dakwaan endorsement. Jangan copy protected logos, artwork, characters atau poster compositions. Escalate legal, regulatory, food-safety atau privacy issues kepada owner yang sesuai.

## Contribution

Cadangkan idea, prompt atau perubahan melalui [CONTRIBUTING.md](CONTRIBUTING.md). Semua perubahan perlu menyatakan scope, owner, version impact dan quality checks.

## Version

Current documentation baseline: **v1.0.0**.

Lihat [CHANGELOG](docs/governance/changelog.md) untuk sejarah perubahan.
