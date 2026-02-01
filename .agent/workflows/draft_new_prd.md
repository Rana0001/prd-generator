---
description: "Interactive workflow to interview the user and draft a new PRD from scratch."
---

# Draft New PRD (Interactive Interview)

This workflow helps you create a robust Product Requirement Document (PRD) by interviewing the user and offering smart suggestions.

## 1. Initial Interview

1.  **Ask**: "What is the name of the product you want to build?"
2.  **Ask**: "Are you building a Mobile App, a Website, or Both?"
3.  **Ask**: "In 1-2 sentences, what is the main problem it solves and who is it for?"
4.  **Wait** for user input.

## 2. Smart Usage & Feature Suggestions

1.  **Analyze** the user's input from Step 1.
2.  **Generate** a list of 3-5 core **Features** that are essential for an MVP of this product.
    - _Constraint_: All 3rd party tool suggestions must be **Free Tier** or **Open Source**.
3.  **Present** these features to the user.
4.  **Ask**: "Do these features look good? Are there any you want to add or remove?"
5.  **Wait** for user approval/edits.

## 3. Tech Stack Recommendation

1.  **Analyze** the requirements.
2.  **Suggest** a recommended **Tech Stack**.
    - _Constraint_: **Strictly prioritize Free Tier / Open Source** (e.g., Supabase Free Tier, Vercel Hobby, PostgreSQL, SQLite, etc.).
    - _Reasoning_: Briefly explain why this stack fits their goal and is cost-effective.
3.  **Ask**: "Does this tech stack work for you? Do you have other preferences?"
4.  **Ask**: "Where do you plan to deploy this? (e.g., Vercel, AWS, App Stores)"
5.  **Wait** for user approval/edits.

## 4. User Flows & Design

1.  **Ask**: "Briefly describe the main user flow. (e.g., 'User signs up -> Creates a Project -> Shares link')."
2.  **Ask**: "Do you have any specific design preferences? (e.g., Minimalist, Dashboard-heavy, Dark mode)"
3.  **Wait** for user input.

## 5. Strategic Planning

1.  **Ask**: "How do you want to phase the delivery? (e.g., MVP features vs Phase 2)"
2.  **Ask**: "What is your Beta Launch plan? (e.g., Internal users first?)"
3.  **Wait** for user input.

## 6. Generate PRD

1.  **Compile** all the gathered information.
2.  **Create** a new file `PRD.md` (or `docs/PRD.md`) using the standard template format.
3.  **Fill** in all sections:
    - **Overview**: From Step 1.
    - **Key Features**: From Step 2.
    - **Technical Architecture & Stack**: From Step 3.
    - **User Flows**: From Step 4.
    - **Strategic Planning**: From Step 5.
    - **Agentic Needs**: Infer these based on the gathered info.
4.  **Notify**: "I have drafted your PRD at `PRD.md`. Please review it."
