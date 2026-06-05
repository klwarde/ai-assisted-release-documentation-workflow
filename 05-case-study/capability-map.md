# Capability map

I designed an AI-assisted documentation workflow for release communication.

It turns release inputs, such as Jira tickets and Git commits, into customer-facing release notes and KB update plans. Validation, editorial judgement, and publishing decisions stay with the technical writer.

| Capability | How this project demonstrates it | Evidence in repo |
|---|---|---|
| Release documentation | Turns mixed product inputs into customer-facing release notes. | `04-final-outputs/final-release-notes.md` |
| Release discovery and triage | Uses AI to identify customer-facing release items from Jira tickets, feature notes, Git commits, and support feedback. | `02-ai-processing/generated-release-contents.md` |
| AI-assisted workflow design | Defines a structured prompt-based workflow with clear inputs, outputs, and validation points. | `prompts/`; `05-case-study/case-study.md` |
| Source analysis | Separates customer-facing changes from internal-only technical details, tests, refactors, and chores. | `02-ai-processing/generated-release-contents.md`; `03-writer-validation/release-contents-validation-notes.md` |
| Documentation judgement | Reviews AI-generated outputs for accuracy, caveats, permission wording, known issue handling, and publishing risk. | `03-writer-validation/release-contents-validation-notes.md`; `02-ai-processing/validation-findings.md` |
| KB impact analysis | Identifies help articles that may need updates, deferrals, or product confirmation. | `04-final-outputs/validated-kb-update-plan.md` |
| Plain language writing | Converts internal release information into clear customer-facing documentation. | `04-final-outputs/final-release-notes.md` |
| Responsible AI use | Treats AI output as draft material and keeps final publishing decisions with the writer. | `03-writer-validation/writer-validation-checklist.md`; `05-case-study/case-study.md` |
| Docs-as-code awareness | Organises source inputs, prompts, outputs, validation notes, and final documentation in a GitHub repository. | Repository folder structure and `README.md` |
| Project management | Uses a WBS tracker, decision log, prompt log, prompt run log, and validation log to manage the work. | `06-project-management/` |
| Project reflection | Identifies workflow limits, future improvements, source quality issues, and process changes. | `05-case-study/case-study.md` |