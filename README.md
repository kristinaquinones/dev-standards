# dev-standards

*This repo holds general, project-agnostic development standards and other reusable workflow/project components that I've found useful. Hopefully it'll prove helpful for you, too.*

✌️ @kristinaquinones

## Overview

This repository is a centralized collection of standards, best practices, and reusable project components that can be applied across multiple software projects and organizations. The standards are designed to be universal and adaptable, providing a solid foundation for establishing consistent practices across teams and disciplines.

## Usage

These standards are designed to be:
- **Project-agnostic**: Applicable to any project or organization regardless of tech stack or industry
- **Reusable**: Copy and adapt sections as needed for your specific project
- **Comprehensive**: Cover all aspects of development, product, marketing, and design
- **Maintainable**: Organized into discrete files for easy updates and navigation

To use these standards in your project:
1. Start with [Philosophy & Principles](philosophy-principles.md) to understand the core values represented in this repo
2. Review the relevant standards index in the appropriate `*-docs/` directory (each contains a README.md)
3. Navigate to relevant sections in the corresponding directories
4. Copy and customize sections as needed for your project
5. Keep project-specific standards in sync with universal standards

## Contents

### Core Philosophy

Before diving into specific standards, start with the [Philosophy & Principles](philosophy-principles.md) document. This outlines the core values that are reflected in this guide.

### Development Standards

Comprehensive development standards for software engineering:

#### **[dev-docs/](dev-docs/)**
  <details>
  <summary>View all topics</summary>

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

  </details>

### Product Management Standards

Product management standards and best practices:

#### **[product-docs/](product-docs/)**
  <details>
  <summary>View all topics</summary>

  - Philosophy & Principles
  - Product Strategy & Vision
  - User Research & Discovery
  - Roadmap Planning
  - Product & Design Process (unified feature definition and design process)
  - Prioritization Frameworks
  - Stakeholder Management
  - Metrics & Success Criteria
  - Release Planning
  - Templates (Product & Design Brief, User Stories)

  </details>

### GTM & Marketing Standards

Go-to-market and marketing standards and best practices:

#### **[gtm-mktg-docs/](gtm-mktg-docs/)**
  <details>
  <summary>View all topics</summary>

  - Positioning & Messaging
  - Channel Strategy
  - GTM Launch Planning
  - Templates (Positioning, Campaign Brief, Messaging Hierarchy, Content Brief)
  
  </details>

### Design Standards

Design standards and best practices:

#### **[design-docs/](design-docs/)**
  <details>
  <summary>View all topics</summary>

  - Information Architecture
  - Interaction Design
  - Usability Evaluation
  - Templates (Design System, Handoff, Usability Testing)
  
  **Note:** For the unified product and design process, see [Product & Design Process](product-docs/product-design-process.md).
  
  </details>

### Measurement & Analytics Standards

Measurement and analytics standards and best practices:

#### **[measurement-docs/](measurement-docs/)**
  <details>
  <summary>View all topics</summary>

  - Analytics Strategy
  - A/B Testing & Experimentation
  - Data Analysis & Interpretation
  - Data Governance
  
  </details>


---

### Repository Structure

```
dev-standards/
├── README.md                    # This file
├── CHANGELOG.md                 # Version history and changes
├── LICENSE                      # GPL v3 license
├── .cursorrules                 # AI assistant rules
├── claude.md                    # Contributor guidelines
├── AGENTS.md                    # Contributing process
│
├── philosophy-principles.md     # Core philosophy and principles
│
├── dev-docs/                    # Development standards
│   ├── README.md                # Development standards index
│   ├── code-organization.md
│   ├── coding-style-standards.md
│   ├── testing-quality.md
│   ├── documentation.md
│   ├── git-version-control.md
│   ├── pull-requests-code-review.md
│   ├── configuration-secrets.md
│   ├── cicd-build-pipeline.md
│   ├── performance-scalability.md
│   ├── accessibility-inclusivity.md
│   ├── security.md
│   ├── architecture-decisions.md
│   └── onboarding-knowledge-transfer.md
│
├── product-docs/                # Product management standards
│   ├── README.md                # Product standards index
│   ├── product-strategy-vision.md
│   ├── user-research-discovery.md
│   ├── roadmap-planning.md
│   ├── product-design-process.md
│   ├── prioritization-frameworks.md
│   ├── stakeholder-management.md
│   ├── metrics-success-criteria.md
│   ├── release-planning.md
│   └── templates/                # Product templates
│       ├── README.md
│       ├── product-design-brief-template.md
│       └── user-story-template.md
│
├── gtm-mktg-docs/              # GTM & Marketing standards
│   └── README.md                # GTM & Marketing standards index
│
├── design-docs/                 # Design standards
│   └── README.md                # Design standards index
│
└── measurement-docs/            # Measurement & Analytics standards
    └── README.md                # Measurement standards index
```

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for the complete contributing process, guidelines, and frequently asked questions.

## Version history

| Version | Date | Contributor | Changes |
|---------|------|-------------|---------|
| 1.0.0 | 2025-12-23 | @kristinaquinones | Initial repository structure with development, product, measurement, design, and GTM standards. |

## License

This repository is licensed under the GNU General Public License v3.0. See [LICENSE](LICENSE) for details.

## Happy building!