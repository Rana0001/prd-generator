---
description: "Workflow to generate Agent Skills, Rules, and Workflows from a filled PRD Template."
---

# Generate Agent Resources from PRD

This workflow guides the agent to read a filled `templates/PRD_TEMPLATE.md` and generate the necessary configuration files for the project.

## 1. Read and Analyze PRD

1. Read the content of `templates/PRD_TEMPLATE.md`.
2. Analyze the requirements, features, and tech stack constraints.

## 2. Suggest Improvements (CRITICAL)

1. Based on the analysis, identify **3-5 missing features or technical improvements** that would verify enhance the product.
2. **CONSTRAINT**: All suggested 3rd party services or tools MUST be **Free Tier compatible** or **Open Source**. Avoid suggesting paid-only enterprise tools.
3. **STOP and Ask the User**: Present these suggestions and ask if they should be included in the scope.

## 3. Generate UI/UX & Flows

1. Create a **Mermaid.js diagram** visualizing the core user flows (e.g., Login -> Dashboard -> Create Item).
2. Write a text-based **Wireframe Description** for key screens, describing layout, components, and interactions.
3. Save this to `docs/USER_FLOWS.md` (create directory if needed).

## 4. Generate Rules

1. Extract strict constraints and guidelines from the "Rules/Guidelines" and "Tech Stack" sections.
2. Create or Update `.agent/rules.md`.
3. Format:

   ```markdown
   # Project Rules

   - [Tech Stack]: Must use <Stack>.
   - [Constraint]: <Constraint>.
   ```

## 5. Generate Skills

1. Identify capabilities required by the "Agentic Needs" section.
2. For each capability, create a file in `skills/<skill_name>.md`.
3. The skill file should contain instructions on how to perform that capability (e.g., "How to query the specific database schema").

## 6. Generate Workflows

1. Identify complex processes from "Workflows Required" or "User Stories".
2. For each process, create a file in `.agent/workflows/<workflow_name>.md`.
3. Follow the standard workflow format (YAML frontmatter + Steps).
