# AI-Assisted Release Documentation Triage Workflow

## Overview

This portfolio project demonstrates an AI-assisted workflow for turning messy product release inputs into validated customer-facing release documentation.

The project uses a fictional SaaS product, **DeskPilot**, and a fictional release, **DeskPilot 2.4**, to simulate a realistic release documentation process.

The workflow focuses on release documentation triage: using AI to help identify customer-facing release items from messy source inputs, then applying technical writer judgement to validate, edit, and prepare final documentation outputs.

## Problem

Release documentation often depends on information scattered across multiple sources: Jira tickets, feature notes, Git commits, support feedback, and product discussions.

In many teams, the technical writer may not receive a clean list of customer-facing release changes. Instead, they need to work out what changed, what matters to users, which internal details should be excluded, which items need validation, and which help articles may need updating.

The hard part is not just writing release notes. The harder part is release triage: turning messy product information into a structured, validated view of what should be communicated.

## Goal

The goal of this project was to design a practical AI-assisted workflow for release documentation.

The workflow needed to show how AI could help with high-volume analysis tasks, such as scanning source inputs, identifying customer-facing changes, excluding internal-only work, surfacing documentation impacts, and producing draft release documentation.

The workflow also needed to preserve the technical writer’s role in validation, editorial judgement, and final publishing decisions.

## Fictional product and release context

**DeskPilot** is a fictional SaaS customer support platform for small and mid-sized businesses. It helps support teams manage customer tickets, automate routine workflows, track service-level targets, and maintain a customer-facing knowledge base.

**Release:** DeskPilot 2.4
**Release theme:** Faster support workflows, clearer automation controls, and improved ticket visibility.

The target users for the release are:

* Support agents
* Support team leads
* Workspace admins
* Customers who submit tickets or use the help centre

## Source inputs

The source pack included four types of messy release input:

* Jira tickets
* Feature notes
* Git commits
* Support feedback

These inputs were intentionally mixed. Some items described customer-facing changes, while others were implementation details, test updates, refactors, chores, or internal monitoring work that should not appear in customer-facing release documentation.

The AI-generated release contents were created from these messy source inputs. A prepared release contents list was not provided as an input.

## Workflow

The workflow was designed as a controlled AI-assisted process, not an automated publishing system.

AI helped process and organise the source material. The technical writer reviewed the output, checked source alignment, resolved uncertainty conservatively, and made the final publishing decisions.

```mermaid
flowchart TD
    A[Messy release source inputs] --> B[P-000: Generate draft release contents]
    B --> C[Writer validates release contents]
    C --> D[P-004: Draft customer-facing release notes]
    C --> E[P-003: Create KB update plan]
    D --> F[P-005: Validate AI-generated documentation outputs]
    E --> F
    C --> F
    F --> G[Validation findings]
    G --> H[Writer review and final edits]
    H --> I[Final release notes]
    H --> J[Validated KB update plan]
    H --> K[Writer validation checklist]
```

### Workflow stages

| Stage                           | Purpose                                                                                                                              | Output                                                                     |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------- |
| Prepare messy source inputs     | Gather Jira tickets, feature notes, Git commits, and support feedback for the release.                                               | Source input files                                                         |
| Generate draft release contents | Use AI to identify customer-facing release items, classify change types, exclude internal-only work, and flag documentation impacts. | Generated release contents                                                 |
| Validate release contents       | Review the generated list for source alignment, missing items, unsupported claims, caveats, and product confirmation needs.          | Release contents validation notes                                          |
| Draft release notes             | Use the generated release contents to create a first-pass customer-facing release note draft.                                        | Draft release notes                                                        |
| Create KB update plan           | Convert documentation impact notes into a structured plan for help article updates, deferrals, and validation needs.                 | Draft KB update plan                                                       |
| Validate AI-generated outputs   | Check generated release contents, draft release notes, and KB plan against the source material and validation notes.                 | Validation findings                                                        |
| Final writer review             | Apply editorial judgement and create the final documentation package.                                                                | Final release notes, validated KB update plan, writer validation checklist |

### Human/AI sequence

```mermaid
sequenceDiagram
    participant Writer as Technical writer
    participant Sources as Messy source inputs
    participant AI as AI prompt workflow
    participant Contents as Generated release contents
    participant Drafts as Draft documentation outputs
    participant Validation as Validation findings
    participant Final as Final documentation package

    Writer->>Sources: Prepare Jira tickets, feature notes, Git commits, and support feedback

    Writer->>AI: Run P-000: Generate draft release contents
    AI-->>Contents: Generated release contents list

    Writer->>Contents: Review source alignment, exclusions, caveats, and validation notes
    Contents-->>Writer: Validated release contents

    Writer->>AI: Run P-004: Draft customer-facing release notes
    AI-->>Drafts: Draft release notes

    Writer->>AI: Run P-003: Create KB update plan
    AI-->>Drafts: Draft KB update plan

    Writer->>AI: Run P-005: Validate AI-generated documentation outputs
    AI-->>Validation: Accuracy, clarity, risk, KB impact, and confirmation findings

    Writer->>Validation: Review findings and decide what to accept, revise, defer, or flag
    Validation-->>Writer: Writer-approved decisions

    Writer->>Final: Apply final edits and prepare documentation package
    Final-->>Writer: Final release notes, validated KB plan, and writer validation checklist
```

## Writer validation

AI-generated content was treated as draft material only.

The validation stage checked whether the generated release contents, draft release notes, and KB update plan were accurate, customer-facing, and safe to use.

The review focused on:

* Whether each release item was supported by the source inputs
* Whether internal-only technical changes had been excluded
* Whether customer impact was explained clearly
* Whether known issues were kept separate from fixes
* Whether wording avoided unsupported claims or overpromising
* Whether permission-related wording could mislead users
* Whether related knowledge base updates had been identified
* Whether any details required product owner or SME confirmation in a real release environment

Because DeskPilot is fictional, product-confirmation issues were handled conservatively. Where the source material did not confirm a detail, I either removed the claim, reworded it more cautiously, or recorded it as a validation note.

## Estimated time impact

For this simulated release, I estimate that the AI-assisted workflow would reduce release documentation preparation time from approximately **7–10 hours** to **4–6 hours**, depending on the quality of the source material and the amount of validation required.

The time saving comes mainly from accelerating the discovery and triage stages: scanning messy source inputs, identifying customer-facing release items, excluding internal-only work, surfacing documentation impacts, and producing a structured release contents list.

The workflow does not remove the need for writer review. Validation, editorial judgement, source alignment, product confirmation, and final publishing decisions remain human responsibilities.

| Activity                                | With AI-assisted workflow | Without AI workflow |
| --------------------------------------- | ------------------------: | ------------------: |
| Review source inputs                    |                30–45 mins |           1–1.5 hrs |
| Generate / create release contents list |                30–45 mins |           1.5–3 hrs |
| Validate release contents list          |              45 mins–1 hr |        45 mins–1 hr |
| Draft release notes                     |                30–45 mins |           1–1.5 hrs |
| Create KB update plan                   |                30–45 mins |           1–1.5 hrs |
| Validate draft outputs against sources  |                 1–1.5 hrs |           1–1.5 hrs |
| Edit final release notes and KB plan    |              45 mins–1 hr |           1–1.5 hrs |
| Prepare final docs/package              |                30–45 mins |          30–45 mins |
| **Total**                               |               **4–6 hrs** |        **7–10 hrs** |

## Final outputs

The final documentation package included:

| Output                                                                                | Purpose                                                                                                                   |
| ------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| [Generated release contents](../02-ai-processing/generated-release-contents.md)       | AI-generated release contents list created from messy source inputs.                                                      |
| [Final release notes](../04-final-outputs/final-release-notes.md)                     | Customer-facing release notes for DeskPilot 2.4, edited after AI drafting and validation.                                 |
| [Validated KB update plan](../04-final-outputs/validated-kb-update-plan.md)           | A writer-reviewed plan showing which help articles should be updated, deferred, or handled with caution.                  |
| [Writer validation checklist](../03-writer-validation/writer-validation-checklist.md) | A reusable checklist for reviewing AI-assisted release documentation before publication.                                  |
| Source input files                                                                    | Fictional Jira tickets, feature notes, Git commits, and support feedback used to simulate a realistic release process.    |
| [Prompt set](../prompts/)                                                             | Structured prompts used to generate release contents, draft release notes, create a KB update plan, and validate outputs. |

Together, these outputs show the full path from messy release inputs to final writer-reviewed documentation.

## What I learned

This project reinforced that AI is most valuable in release documentation when it supports structured thinking rather than replacing judgement.

### Project management

During the prototype, I initially used a single Excel workbook to manage planning, source inputs, prompts, outputs, and validation notes. As the project expanded, the workbook became harder to navigate.

In a future version, I would keep the workbook as a lightweight project tracker only, and manage source inputs, prompts, AI outputs, and final documentation as separate files in the repository from the start.

### Strongest use case

The strongest use case was not simply **drafting release notes**. It was **release discovery and triage**: identifying customer-facing changes from messy inputs, excluding internal-only work, grouping related updates, and surfacing documentation impacts.

The generated release contents table also became the central source for the rest of the workflow. Because it already identified the main release items, change types, customer impacts, documentation impacts, and validation notes, I could use it directly to draft release notes and plan KB updates rather than adding extra intermediate analysis steps to, say, extract-and-group data from the source inputs.

This is where AI was most useful, because it helped **turn scattered source material into a structured release view that a writer could review and refine**.

### AI limits

The project also showed the limits of AI. The generated outputs still needed human review to check source alignment, remove unsupported claims, clarify permission wording, keep known issues separate from fixes, and flag details that would require product confirmation.

AI could accelerate the analysis and drafting work, but it could not confirm product behaviour or make final publishing decisions.

### Hybrid workflow

A useful AI-assisted workflow does not need to be fully automated to be valuable.

A controlled manual workflow, using structured prompts and clear validation steps, can still improve documentation speed while preserving editorial control.

## Future improvements

In a real documentation environment, I would extend the workflow by providing previous release note examples, an approved documentation style guide, product terminology, and existing KB article samples.

These inputs would help the AI follow the company’s preferred structure, tone, terminology, and level of detail more closely.

I would also test the workflow with larger and messier release inputs to understand where the process scales well and where additional human review, source tagging, or prompt refinement would be needed.

## What this demonstrates

This project demonstrates my ability to:

* Design a practical AI-assisted documentation workflow
* Use AI to support release discovery and triage
* Translate messy product inputs into clear customer-facing release documentation
* Maintain a high velocity of documentation updates without bypassing review
* Separate customer-facing changes from internal technical detail
* Identify related knowledge base impacts from release changes
* Validate AI-generated content against source material
* Apply editorial judgement to reduce ambiguity, overclaiming, and publishing risk
* Preserve human ownership of final documentation decisions

The project is intentionally scoped as a workflow prototype rather than a full automation tool. This keeps the focus on documentation judgement, process design, and responsible AI use.
