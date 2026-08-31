---
title: DOHNUT Source Artifact Inventory
 date: 2026-08-31
version: 1.0.0
author: DOHNUT / GangNiaga Sdn. Bhd.
status: draf
tags: [governance, assets, source-artifacts]
related_documents:
  - ../00-system-index.md
  - ../visual-ai/visual-ai-engine-v1.0.0.md
---

# DOHNUT Source Artifact Inventory

## Purpose

Dokumen ini merekodkan semua bahan sumber yang telah dibangunkan sepanjang pembangunan DOHNUT Creative OS dan membezakan **canonical text documentation** daripada **binary presentation/source artifacts**.

## Canonical text sources

| Category | Canonical repository location |
|---|---|
| Brand constitution | `docs/brand/brand-constitution-v1.0.0.md` |
| DOH Language | `docs/creative/doh-language-v1.0.0.md` |
| DOH Cinema | `docs/creative/doh-cinema-v1.0.0.md` |
| Doh Boy | `docs/creative/doh-boy-v1.0.0.md` |
| Pop Culture Playbook | `docs/creative/pop-culture-playbook-v1.0.0.md` |
| Visual AI Engine | `docs/visual-ai/visual-ai-engine-v1.0.0.md` |
| Creative Genome | `docs/visual-ai/creative-genome-v1.0.0.md` |
| Google Flow prompt template | `docs/visual-ai/google-flow-prompt-template-v1.0.0.md` |
| Prompt Registry | `docs/prompt-registry.yaml` |
| Prompt System | `docs/ai/prompt-system-v1.0.0.md` |
| Skills Matrix | `docs/ai/skills-matrix-v1.0.0.md` |
| System Index | `docs/00-system-index.md` |

## Source artifacts created during the project

The working session produced these binary/source artifacts:

- `DOH-NUT_Brand_Guidelines_A-Z.pdf`
- `DOH-NUT_Brand_Guidelines_A-Z.docx`
- `DOHNUT_Pop_Culture_Playbook_v1.0.docx`
- `DOHNUT_Pop_Culture_Playbook_v1.0.pdf`
- `dohnut-ai-documentation-v1.0.0.zip`
- `dohnut-visual-ai-engine-v1.0.0.zip`
- DOHNUT brand board / logo / packaging / pattern / social reference images
- Google Flow chocolate-hazelnut visual reference

## Ingestion policy

Text-native documentation is canonical and should be edited in Git. Binary source artifacts should be stored in a binary-capable asset store or attached to a GitHub Release / Git LFS when repository-side binary upload is operationally available.

## Integrity rule

Do not silently replace a source artifact with a screenshot or a lossy derivative. Preserve original filenames, source provenance, version, and checksum when binary ingestion is completed.
