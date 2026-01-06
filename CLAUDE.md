# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the EdgeFlow documentation site built with Mintlify. EdgeFlow is a behavioral preference assessment application.

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
├── docs/               # Documentation
│   ├── index.mdx       # Overview
│   ├── installation.mdx
│   ├── quickstart.mdx
│   ├── concepts/       # Core methodology
│   ├── guide/          # User workflows
│   ├── hardware/       # Arduino setup
│   ├── settings/       # Configuration
│   └── troubleshooting/
└── resources/          # Resources (media, downloads)
    ├── index.mdx       # Resources overview
    ├── setup-examples.mdx
    ├── demos.mdx
    └── downloads.mdx
```

## Navigation Structure

Navigation is defined in `docs.json` under `navigation.tabs`. Two main tabs:

**Documentation tab:**
- Getting Started (overview, installation, quickstart)
- Core Concepts (assessments, stimuli, ranking, correspondence)
- User Guide (participants, sessions, assessments, results, export)
- Hardware Setup (requirements, connection, calibration)
- Configuration (assessment, display, data)
- Troubleshooting (common-issues, faq)

**Resources tab:**
- Setup Examples (hardware wiring, configuration examples)
- Demo Videos (walkthroughs, tutorials)
- Downloads (stimulus libraries, sample data, templates)

## EdgeFlow Context

EdgeFlow is a Tauri v2 desktop app (React + Rust) for behavioral research:
- **VMSWO**: Verbal multiple stimulus without replacement preference assessment (uses "selections" not "trials")
- **Conjugate Reinforcement**: Force-based behavioral engagement via Arduino Nano + IPS121C dynamometer
- **Correspondence Analysis**: Comparing verbal and behavioral preference measures

Hardware: Arduino Nano (USB-C) with Vernier IPS121C dynamometer on pin A7, 9600 baud, 20Hz sampling.

Reference: Sheridan et al. 2024 methodology

## Writing Style

- Clean, professional tone suitable for research/clinical audience
- Use Mintlify components: Cards, Steps, Accordions, Tabs, Notes, Tips, Warnings
- Required frontmatter: `title`, `description`, `icon`
- Avoid gradients or overly flashy styling
