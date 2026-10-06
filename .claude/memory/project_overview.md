---
name: project-overview
description: SDD Cookbook - Framework for Software Design Documents in agent-based development for IT products
metadata:
  type: project
---

**Project**: SDD Cookbook - Comprehensive SDD Framework for Agent-Based Development

## Core Purpose
SDD Cookbook defines a standardized framework for describing Software Design Documents (SDD) within the context of **agent-based development** when creating IT products. It establishes both universal practices (using unified agents) and team-specific implementations (using concrete agents).

## Architecture
- **Tool**: Currently OpenSpec (@fission-ai/openspec), extensible for future tools
- **Language**: Russian
- **Format**: Markdown files in Obsidian vault
- **Version Control**: Git-backed with automatic vault backups

## Four Main Sections

1. **Roles** (`OpenSpec/roles/`)
   - Defines team member activities by role
   - Clarifies responsibilities, authorities, and workflow participation
   - Examples: developers, QA engineers, system analysts

2. **Store** (`OpenSpec/store/`)
   - Feature lifecycle documentation from business signal to production
   - Knowledge base of best practices and procedures
   - Complete flow: inception → decision → implementation → production merge

3. **Gates** (`OpenSpec/gates/`)
   - Boundary cases and edge situations in SDD process
   - Quality checkpoints and exception handling
   - Examples: mid-development documentation changes, problem discovery

4. **Cases** (`OpenSpec/cases/` - planned)
   - Real-world implementation cases with specific team details
   - Describes team-specific conventions, fields, and adaptations
   - Includes improvement initiatives for agent-based development

## Key Principle
**Unified Agent** → general information
**Specific Agent** → concrete team cases with peculiarities and field-level details
