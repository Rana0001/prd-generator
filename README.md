# PRD & Agent Resource Generator

This project is a toolkit designed to help you quickly generate robust **Product Requirement Documents (PRDs)** and subsequently configure **AI Agent Resources** (Skills, Workflows, Rules) to build your project.

## Overview

The goal is to streamline the "Planning" and "Agent Configuration" phases of development. Instead of writing everything from scratch, you can use the provided workflows to:

1.  **Draft a PRD**: Interactively interview with an AI to clarify your idea and generate a structured PRD.
2.  **Generate Resources**: Use the PRD to automatically generate the necessary instructions, specific skills, and workflows for your AI coding agent.

## Workflows

This project includes pre-defined workflows located in `.agent/workflows`.

### 1. Draft New PRD

**Command**: `/draft_new_prd`
**File**: `.agent/workflows/draft_new_prd.md`

Use this workflow to start a new project. The agent will:

- Interview you about your product idea.
- Suggest features and open-source tech stacks.
- Plan your **Strategic Delivery** (Phases, Beta Launch) and **Deployment**.
- Draft a `PRD.md` file for you.

### 2. Generate Agent Resources

**Command**: `/generate_agent_resources`
**File**: `.agent/workflows/generate_agent_resources.md`

Once you have a filled `templates/PRD_TEMPLATE.md` (or the one generated from the previous step), use this workflow. The agent will:

- Analyze your PRD.
- Suggest missing technical features.
- Generate specific **Skills** (`skills/*.md`) tailored to your project.
- Generate **Workflows** (`.agent/workflows/*.md`) for complex processes.
- Set up **Rules** (`.agent/rules.md`) that enforce:
  - **Clean Architecture, SOLID, and DRY** principles.
  - **15 Golden UI/UX Principles** (Clarity, Speed, Accessibility, etc.).

## Project Structure

- **`.agent/workflows`**: Contains the interactive workflows for the agent.
- **`instructions`**: Guides on how to use this repository with other AI models (e.g., manually pasting prompts).
- **`skills`**: Directory to store generated agent skills.
- **`templates`**: Contains the `PRD_TEMPLATE.md` used as the source of truth.

## Manual Usage / Other Agents

If you are not using an agent with workflow capabilities, you can follow the manual instructions in:
`instructions/RUN_WITH_OTHER_AGENTS.md`

This file contains specific prompts you can copy-paste into ChatGPT, Claude, or other LLMs to achieve similar results.
