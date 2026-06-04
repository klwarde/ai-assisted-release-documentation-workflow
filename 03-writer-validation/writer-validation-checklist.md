# Writer validation checklist

This checklist was used to review AI-assisted release documentation outputs before treating them as final.

The purpose is to show where human judgement is required: checking source alignment, removing unsupported claims, clarifying customer impact, separating known issues from fixes, validating KB impacts, and identifying details that would require product or SME confirmation in a real release environment.

| Check area | Validation question | Applies to | Why it matters | Pass / Needs review | Notes |
|---|---|---|---|---|---|
| Source alignment | Does each release item match the Jira tickets, feature notes, commits, or support feedback? | Generated release contents | Prevents unsupported or inaccurate release items from entering the workflow. |  |  |
| Customer relevance | Is the change meaningful to customers or users? | Generated release contents; release notes | Prevents internal-only work from appearing in customer-facing release notes. |  |  |
| Internal-only exclusions | Have refactors, tests, chores, monitoring, and implementation-only changes been excluded? | Generated release contents | Keeps the release contents focused on customer-facing change. |  |  |
| Change classification | Are features, improvements, fixes, admin updates, and known issues classified correctly? | Generated release contents; release notes | Helps structure the release notes clearly. |  |  |
| Affected users | Are the correct user groups identified? | Generated release contents; release notes; KB plan | Helps users understand whether the change applies to them. |  |  |
| Customer impact | Is the user benefit or behaviour change explained clearly? | Generated release contents; release notes | Makes release notes useful rather than just descriptive. |  |  |
| Plain language | Is the wording clear, specific, and customer-facing? | Release notes; KB plan | Keeps the documentation readable and useful. |  |  |
| Unsupported claims | Does the wording avoid unverified claims, metrics, or performance promises? | Release notes; KB plan | Reduces publishing risk. |  |  |
| Permission wording | Does the wording avoid implying access that may depend on user role or permissions? | Release notes; KB plan | Prevents confusion around admin-controlled features. |  |  |
| Known issue handling | Are known issues separate from fixes and improvements? | Generated release contents; release notes | Prevents users from misunderstanding unresolved issues as resolved. |  |  |
| KB impact | Have affected help articles been identified and prioritised appropriately? | KB update plan | Connects release communication to wider documentation maintenance. |  |  |
| Product confirmation | Are uncertain details flagged for product owner or SME confirmation? | Generated release contents; release notes; KB plan | Shows what would need validation in a real release. |  |  |
| Final approval | Has the writer reviewed and approved the final wording? | Final release notes; validated KB plan | Confirms the output is not treated as raw AI-generated content. |  |  |