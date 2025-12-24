# Changelog

All notable changes to this repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2025-12-23


### Changed
- Consolidated `feature-definition-requirements.md` and `user-centered-design-process.md` into unified `product-design-process.md` in `product-docs/`
- Merged `prd-template.md` and `design-brief-template.md` into unified `product-design-brief-template.md` in `product-docs/templates/`
- Updated all cross-references across repository to reflect consolidation
- Updated `product-docs/README.md` and `design-docs/README.md` to reflect new structure
- Design-docs now focuses on specialized frameworks (Information Architecture, Interaction Design, Usability Evaluation) while product-docs contains the unified process

### Removed
- `product-docs/feature-definition-requirements.md` (consolidated into `product-design-process.md`)
- `design-docs/user-centered-design-process.md` (consolidated into `product-design-process.md`)
- `product-docs/templates/prd-template.md` (consolidated into `product-design-brief-template.md`)
- `design-docs/templates/design-brief-template.md` (consolidated into `product-design-brief-template.md`)

### Added
- Initial version of development standards extracted from EmberDocs project standards
- Reorganized development standards into discrete files in `dev-docs/` directory with `dev-docs/README.md` as index
- Created comprehensive documentation structure with 15 individual standard files:
  - Philosophy & Principles
  - Code Organization
  - Coding Style & Standards
  - Testing & Quality
  - Documentation
  - Git & Version Control
  - Pull Requests & Code Review
  - Configuration & Secrets
  - CI/CD & Build Pipeline
  - Performance & Scalability
  - Accessibility & Inclusivity
  - Security
  - Architecture Decisions
  - Onboarding & Knowledge Transfer
  - Sync Instructions for .cursorrules, claude.md, AGENTS.md
- Added `.cursorrules`, `claude.md`, and `AGENTS.md` for documentation repository standards
- Created placeholder structure for GTM & Marketing standards (`gtm-mktg-docs/README.md`)
- Created placeholder structure for Product Management standards (`product-docs/README.md`)
- Created placeholder structure for Design standards (`design-docs/README.md`)
- Added CHANGELOG.md to track version history
- Added collapsible section guidelines for long lists in README and index files

### Changed
- Moved all standards index files to their respective folders as README.md files (following GitHub conventions)
- Updated README.md with new repository structure, expanded scope including all standards sections, and folder-based navigation
- Reorganized README.md structure to include all standards types (Development, Product, GTM & Marketing, Design)
- Updated documentation standards to include collapsible section best practices

[1.0.0]: https://github.com/yourusername/dev-standards/releases/tag/v1.0.0
