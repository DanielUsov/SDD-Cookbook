# SDD Cookbook

## Project Overview
SDD Cookbook is a comprehensive framework for describing **Software Design Documents (SDD)** in the context of **agent-based development** for IT products. It defines standardized approaches to software design, team workflows, and implementation cases using unified and specific agents.

## Framework Principles

### Core Concept
- **Unified Agent**: Used for general/common information about software development practices
- **Specific Agent**: Used when describing concrete implementation cases with team-specific details, fields, and peculiarities
- **Tool Integration**: Currently using **OpenSpec** (@fission-ai/openspec), with support for additional tools in the future

## SDD Structure

The framework is organized into four main sections within `OpenSpec/`:

### 1. **Roles** (`roles/`)
Describes activities and responsibilities of team members based on their role:
- Developers (Разработчик)
- QA/Testers (Тестировщик)
- System Analysts (Системный аналитик)
- Other specialized roles

Each role definition clarifies responsibilities, decision-making authority, and specific activities within the SDD process.

### 2. **Store** (`store/`)
Documents the complete lifecycle of a feature from inception to production:
- **Beginning**: Business signal, intent, decision
- **Development**: Implementation process
- **Integration**: Code merge to production/master branch
- **Completion**: Feature deployment

This section serves as the knowledge base for feature lifecycle management.

### 3. **Gates** (`gates/`)
Describes boundary cases and edge situations that may occur during the SDD process:
- Documentation changes during development
- Problem discovery and remediation
- Quality checkpoints and approvals
- Exception handling procedures

### 4. **Cases** (`cases/` - future)
Real-world implementation cases describing:
- Specific team implementations on actual projects
- Team-specific peculiarities, fields, and conventions
- Custom workflows and adaptations
- **Initiatives**: Proposals for improvements and perspectives on agent-based development evolution

## Key Information
- **Main Directory**: `OpenSpec/`
- **Language**: Russian
- **Format**: Markdown (Obsidian Vault)
- **Version Control**: Git-backed with automatic vault backups
- **Current Tools**: OpenSpec (@fission-ai/openspec)
- **Future**: Support for additional tools and frameworks

## Working with Claude

### Common Tasks
1. **General Documentation**: Edit framework guidelines using unified agent perspective
2. **Implementation Cases**: Describe specific team practices with concrete agent details
3. **Content Organization**: Maintain consistency across roles, gates, store, and cases sections
4. **Knowledge Management**: Structure and refine technical specifications and workflows

### Important Notes
- Content is in Russian
- Markdown-based, Obsidian-compatible
- Focus on agent-based development practices
- Support for multiple implementation tools/frameworks
- Emphasis on team-specific adaptations and improvement initiatives

### Memory
Claude will maintain project context in `.claude/memory/` to improve future interactions and understand framework nuances.
