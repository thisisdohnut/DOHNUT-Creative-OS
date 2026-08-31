# Changelog

## [1.2.0] — 2026-08-31

### Added

- Unified root `PRD.md` for product requirements and acceptance criteria.
- Unified root `ARCHITECTURE.md` for commerce, Creative OS, ERP and AI runtime boundaries.
- Unified root `DESIGN.md` for ecommerce + Creative Studio UX/UI standards.
- Unified root `ERP.md` for operational business systems.
- Unified root `PROMPT.md` for prompt engineering, Creative Genome, routing and provider adapter contracts.
- `INTEGRATION-E-COMMERCE.md` defining the integration contract with `thisidowgnut-source/Dowgnut-Custom`.

### Changed

- README now presents DOHNUT-Creative-OS as the canonical creative/intelligence layer and `Dowgnut-Custom` as the ecommerce/application layer.
- System Index upgraded to version 1.2.0 and links the unified project documents.

### Integration Note

The target architecture is a governed system-of-systems. The Creative OS repository does not blindly absorb the ecommerce application code. The application repository remains authoritative for customer commerce, order, payment and inventory runtime.

The current GitHub connection has read-only access to `thisidowgnut-source/Dowgnut-Custom`; therefore no code was written into that repository from this session. The integration contract is committed here so implementation can proceed without architecture drift.

## [1.1.0] — 2026-08-31

### Added

- GitHub-ready Markdown authoring standard based on GitHub Flavored Markdown practices.
- Dedicated Quality Gates document with scoring and release thresholds.
- Source of Truth hierarchy and status model.
- Asset Registry contract and creative lineage model.
- Provider-agnostic AI architecture with routing and fallback principles.
- Root README visual system overview using a repository-local SVG.
- Contribution protocol.
- CODEOWNERS and pull request / issue templates.

### Changed

- System Index upgraded to describe Provider Adapter, Asset Registry and executable QA layers.
- README upgraded with visual navigation, Quick Start, Visual North Star and module map.

## [1.0.0] — 2026-08-31

### Added

- DOHNUT Creative OS repository foundation.
- Brand Constitution.
- DOH Language™ system and phrase bank.
- DOH Cinema™ and DOHFLIX™ concepts.
- Doh Boy™ character bible with 20 personality modes.
- Pop Culture Playbook™ with parody titles, DOH copy, Malaysian references, campaigns, packaging, OOH and TikTok hooks.
- Visual AI Engine™ architecture.
- Creative Genome schema.
- Structured AI Prompt System.
- Skills Matrix.
- Data Contracts.
- Governance, quality gates, controlled glossary and IP/parody guardrails.

### Notes

Future changes must use semantic versioning and update cross-references plus this changelog.
