# Audit finding closure evidence

When an owner says an audit finding is fixed, the compliance lead gets the finding, the promised actions and the records supplied side by side: what each promise is backed by, what is missing and the questions to settle first. The auditor or the compliance lead decides whether it closes.

*Workflow template · Compliance, risk and privacy · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/audit-finding-closure-evidence/)*

## The outcome

"Done, please close it" is a message every compliance lead knows, and one of the slowest to check. The action plan promised particular evidence. The owner sends a folder of attachments. Somebody has to line the two up, notice the month with no sign-off, the second system nobody mentions and the email standing in for a change record, and then chase each gap.

This workflow template does that lining up in one pass. Every item of evidence the plan promised sits beside the records tied to it, with one of three outcomes: supplied as promised, partly supplied or not supplied. A record counts only when it is dated no earlier than the day the finding was raised, is not dated in the future, and is the kind the plan promised: a revised document, a record that the change was made, or records the fixed control produced as it ran. An owner's own email that the work is done is listed, but it never stands in for a record. Gaps in time (for promises with a period) and gaps in scope (for implementation and operation promises) are named, so "the check has run since August" becomes "no record covers September".

The comparison ends with retest questions for the person who decides closure, and a numbered list of questions, each addressed to the person who can answer it. It never says the finding is closed, that the fix works or that a requirement is met. For the index of everything an auditor asks to see before an audit, use [Audit evidence index](https://fullypowered.ai/workflows/audit-evidence-index/); for investigating an incident and following its actions, use [Incident investigation and corrective actions](https://fullypowered.ai/workflows/incident-investigation-and-corrective-actions/).

## Who starts the work, and when

The compliance lead starts it when the owner of a finding reports the agreed actions complete and sends the records, before the finding goes to the person who decides closure. The action owner can run it first, before submitting, to find the gaps while they are still theirs to fill. It runs again when the owner answers the questions with more records.

The person who decides closure is named in the settings: by default the auditor who raised the finding, whether internal audit, an external auditor or a customer, or the compliance lead for an issue the company found itself.

## What they supply

- **The finding record** from the findings tracker: what was found, the requirement it was measured against, the recorded cause, the rating, who raised it and when, and the systems, sites or teams it covers.
- **The agreed action plan,** one row for each item of evidence promised, with the action, its owner, its due date, the kind of evidence promised, its scope and, for a control that runs over time, the period it should cover.
- **The owner's response** as received, with who sent it and the date.
- **The evidence list,** one row for each record supplied, saying which promise it answers, its kind and date, the period and scope it covers, and where it is kept.
- **A few settings:** today's date, the compliance lead and who decides closure.

Both exports are read by set column headers. If a header does not match, the assistant stops and asks which column is which. It opens no evidence file and needs no connection to the tracker or any other system.

## What comes out

One comparison in a fixed order. It opens with the finding as recorded and two count lines that add up: the promised items by outcome, and the records counted, not counted and tied to no promise. It says which parts of the finding's scope no promised item reaches.

Then each action in plan order, with what the owner reported and any note (reported by someone other than its owner, past due, reported done after the due date), and under it each promised item with its outcome, the records counted, the records not counted with the reason, and exactly what is missing. Records tied to no promise come next, then the retest questions, the questions before the closure decision and the decisions kept for people. Every empty section says so.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), where findings from every kind of audit are tracked to closure.
- [Information security](https://fullypowered.ai/functions/information-security/), where many findings are about access, change and monitoring controls that must be shown to run over time.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), where internal audit, external auditors and examiners all raise findings that need closing on records.
- [Insurance](https://fullypowered.ai/industries/insurance/), where audit committees follow overdue and reopened findings closely.
- [Software technology](https://fullypowered.ai/industries/software-technology/), where customer security audits and annual attestation work raise findings on systems that change every week.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the first serious audit arrives and nobody has closed a finding on records before.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the findings tracker is long and the same findings come back year after year.

## What has to change for your company

Map your findings tracker and evidence log to the column headers once, so every run starts from the same exports. Decide who closes each kind of finding: internal audit, the external auditor, a customer, or the compliance lead for an issue found internally. Agree the kinds of evidence your auditors expect and whether a signed attestation from a named officer may ever count; as written, an owner's own account counts only where the plan promised one. Decide whether evidence dated before the finding may count for work already under way; as written it never does. Name who sends the approved comparison to the owner or the auditor, and who updates the tracker. It runs in ChatGPT, Claude, Copilot or Gemini from the exports and notes you supply. Questions about what a law or regulation requires go to counsel; the comparison interprets none.

## What has been checked

Fully Powered AI wrote this workflow template. It was editorially reviewed on 11 November 2026. It was tried on its invented example in Claude on 11 November 2026, in two runs: an independent review changed the instruction block after the first, and the record of both is published with it. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on two or three findings your compliance lead has already closed or sent back, plus cases written in advance, each with its expected result: an email standing in for a change record, a month with no sign-off, a second system with no record, a record tied to no promise, a header renamed in the export. The compliance lead checks every outcome against the files themselves before anyone relies on the comparison. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by Fully Powered AI.
- Sources and rights reviewed.
- Editorially reviewed on 11 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 11 November 2026. The record is in [TRIAL.md](TRIAL.md).
- Not yet tested in a client environment.

## What is in this folder

- [TEMPLATE.md](TEMPLATE.md): the complete workflow template. Roles, inputs, the procedure, exceptions and stop conditions, the output format, a reviewer checklist, acceptance tests, the instructions for an AI assistant and what to customize.
- [EXAMPLE.md](EXAMPLE.md): a worked example with invented data.
- [TRIAL.md](TRIAL.md): what came out when the template was tried on its example.
- [SKILL.md](SKILL.md): the technical file, for AI products that load packaged instructions from a folder.
- [SOURCES.md](SOURCES.md): what the workflow template drew on, with licences.
- [LICENSE](LICENSE): MIT. Use it, change it, make it yours.

## Start using it

1. Read [EXAMPLE.md](EXAMPLE.md) to see what a good result looks like.
2. Open [TEMPLATE.md](TEMPLATE.md) and set every item under "What to customize" to your own rules, roles and limits.
3. Give your AI assistant the instruction block and the output format from the template, with your own limits in place of the ones the instructions leave open in square brackets. Paste them in as custom instructions in ChatGPT, Claude, Copilot or Gemini, or copy this whole folder into a product that loads `SKILL.md` packages. This folder stands alone; you do not need the rest of the repository.
4. Run it on past work first, using the reviewer checklist and acceptance tests in the template, before anyone relies on it.

## Related workflow templates

- [Audit evidence index](https://fullypowered.ai/workflows/audit-evidence-index/)
- [Incident investigation and corrective actions](https://fullypowered.ai/workflows/incident-investigation-and-corrective-actions/)
- [Audit preparation](https://fullypowered.ai/workflows/audit-preparation/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
