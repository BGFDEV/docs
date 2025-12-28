# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is BGF Development's documentation site built with Mintlify. It currently documents EdgeFlow, a behavioral preference assessment application.

## Commands

```bash
# Install Mintlify CLI globally
npm i -g mint

# Start local dev server (runs at http://localhost:3000)
mint dev

# Update CLI if dev environment issues occur
mint update

# Check for broken links
mint broken-links
```

## Architecture

```
/
├── docs.json           # Site configuration, navigation, theme
├── index.mdx           # Landing page
└── edgeflow/           # EdgeFlow documentation
    ├── index.mdx       # Overview
    ├── installation.mdx
    ├── quickstart.mdx
    ├── concepts/       # Core methodology
    ├── guide/          # User workflows
    ├── hardware/       # Arduino setup
    ├── settings/       # Configuration
    └── troubleshooting/
```

## Navigation Structure

Navigation is defined in `docs.json` under `navigation.tabs`. The EdgeFlow tab contains groups:
- Getting Started (overview, installation, quickstart)
- Core Concepts (assessments, stimuli, ranking, correspondence)
- User Guide (participants, sessions, assessments, results, export)
- Hardware Setup (requirements, connection, calibration)
- Configuration (assessment, display, data)
- Troubleshooting (common-issues, faq)

## EdgeFlow Context

EdgeFlow is a Tauri v2 desktop app (React + Rust) for behavioral research:
- **VMSWO**: Verbal multiple stimulus without replacement preference assessment
- **Conjugate Reinforcement**: Force-based behavioral engagement via Arduino dynamometer
- **Correspondence Analysis**: Comparing verbal and behavioral preference measures

Reference: Sheridan et al. 2024 methodology

## Writing Style

- Clean, professional tone suitable for research/clinical audience
- Use Mintlify components: Cards, Steps, Accordions, Tabs, Notes, Tips, Warnings
- Required frontmatter: `title`, `description`, `icon`
- Avoid gradients or overly flashy styling
