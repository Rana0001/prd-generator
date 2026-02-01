# Using the PRD Template with Other AI Agents (ChatGPT, Claude, etc.)

You can use the `templates/PRD_TEMPLATE.md` with any powerful LLM to jumpstart your project. Here are the prompts to use.

---

## Step 1: Ingest, Analyze & Suggest

**Action**: Copy the filled content of `templates/PRD_TEMPLATE.md`.
**Prompt**:

> I am building a software application. Here is my Product Requirement Document (PRD).
>
> **Your Task:**
>
> 1.  **Analyze** the requirements deeply.
> 2.  **Critique & Suggest**: Propose 3-5 missing features, technical improvements, or edge cases I missed. **IMPORTANT: Suggest ONLY Free Tier or Open Source solutions.** Explain WHY they are important.
> 3.  **Visual Flow**: Generate a Mermaid.js diagram code showing the main user journey.
> 4.  **UI/UX**: Describe the wireframe for the top 3 most important screens in text format.
>
> **[PASTE PRD CONTENT HERE]**

---

## Step 2: Generate "Skills" (Agent Instructions)

**Action**: After refining the PRD with the agent from Step 1.
**Prompt**:

> Based on the finalized PRD, I want to configure an AI Agent to help me build this.
>
> **Your Task:**
> Identify specific "Skills" (capabilities) the agent needs (e.g., "How to use the Database", "How to run tests", "How to deploy").
>
> For EACH skill, generate a Markdown file content following this format:
>
> `skills/<skill_name>.md`
>
> ```markdown
> ---
> name: [Skill Name]
> description: [Short description]
> ---
>
> # [Skill Name] Instructions
>
> 1. [Step 1]
> 2. [Step 2]
> ```

---

## Step 3: Generate Workflows

**Action**: To define multi-step processes.
**Prompt**:

> Now, identify complex, multi-step **Workflows** that occur in this project (e.g., "User Onboarding", "Database Migration", "Release Process").
>
> For EACH workflow, generate a Markdown file content following this format:
>
> `.agent/workflows/<workflow_name>.md`
>
> ```markdown
> ---
> description: [Short description]
> ---
>
> # [Workflow Name]
>
> 1. [Step 1]
> 2. [Step 2]
> ```

---

## Step 4: Generate Rules

**Action**: To set boundaries.
**Prompt**:

> Finally, generate a `.agent/rules.md` file that strictly defines the Tech Stack, Coding Standards, and any "Do Nots" from the PRD.
>
> Format:
>
> ```markdown
> # Project Rules
>
> - Always use [Tech Stack]
> - Never [Prohibited Action]
> ```
