# Obligation and filing calendar review

Before each scheduled review, the compliance lead, company secretary or environmental lead sees what comes due from the organisation's own register: each obligation, filing and renewal with its owner, its due date as recorded, the evidence on file and every gap as a question. It works out no deadline and files nothing.

*Workflow template · Compliance, risk and privacy · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/obligation-and-filing-calendar-review/)*

## The outcome

The review starts from one list instead of a spreadsheet and a memory. Every obligation in the window is there in date order: the annual reports for each company in the group, the licence and certificate renewals, the permit reports and monitoring rounds. Each line shows who owns it, the due date exactly as the register holds it, what evidence of completion the register asks for and what is actually on file.

The problems that usually surface the week something is due are on the page months before: a monitoring round with no owner, an owner who has left, a report whose recorded date has passed with no evidence on file, a registry reminder that gives a different date from the register, an entry nobody has verified for well over a year. Each one arrives as a numbered question addressed to the person who can answer it.

The register stays the only authority. The workflow template works out no deadline, from a law, a frequency or last year's date, and adds no obligation the register does not hold, even when a notice or a stray piece of evidence suggests one. It gives no legal advice, has not been reviewed by a lawyer, and never says whether a duty applies or has been met: counsel, or the specialist who verifies the register, decides that. It files, submits, pays and sends nothing, and changes nothing in the register.

## Who starts the work, and when

The compliance lead, the company secretary or the environmental lead starts it when the agreed review of the register is due: monthly or quarterly for most organisations, and before a board meeting, an audit or a change of owner. Each can run it on their own part of the same register: the company secretary on entity filings, the environmental lead on permit and monitoring duties, the compliance lead on all of it.

The reviewer reads the list and sets priorities. Counsel, or the specialist named in the register, answers the questions about dates and verification. The owners do the work and keep the evidence.

## What they supply

- **The obligation register,** exported with its standard columns: each obligation, its kind, the company or site, the body it is owed to, the owner, the due date, the frequency, the evidence required, and who verified the entry and when. If the column headers differ, the workflow template stops and asks.
- **The evidence log,** if one is kept: each piece of evidence of completion, the obligation and due date it answers, where it is kept and who recorded it.
- **The notices received:** reminders and letters from registries, agencies, licensing offices or a registered agent, with the date each states.
- **A few settings:** today's date, the window (90 days unless changed), the scope, the reviewer, who verifies when the register does not say, how often an entry should be verified again (12 months unless changed), and the list of current owners.

## What comes out

One list, marked as a draft for the reviewer, in a fixed order:

- **Past recorded due date, no evidence on file.**
- **Coming due in the window,** earliest first, with the days to each recorded date.
- **Past recorded due date, evidence on file,** where the register has not yet been given the next date.
- **No usable due date.**
- **Notices that do not match the register,** with both dates side by side and neither chosen, and notices for nothing in the register, with nothing added.
- **Evidence not placed:** evidence recorded against an obligation the register does not hold.
- **Questions,** numbered, each addressed to the owner, the reviewer or the person who verifies the register.
- **Also noted:** what is due after the window, evidence for an earlier due date, and notices that agree with the register.

A group with nothing in it says "None." Every line can be checked against the register, and the header counts add up to the rows in scope.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), which keeps the register of what the organisation owes, to whom and by when.
- [Legal and contracts](https://fullypowered.ai/functions/legal-and-contracts/), where the company secretary keeps each company's annual filings in order and counsel verifies what is owed.
- [Health, safety and environment](https://fullypowered.ai/functions/health-safety-and-environment/), where the environmental lead tracks permit reports and monitoring rounds and the evidence each one leaves.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where a plant carries permits, inspections and licence renewals on many different cycles.
- [Energy](https://fullypowered.ai/industries/energy/), where sites report monitoring results and renew registrations to several agencies at once.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), where a group of companies and registrations each carries its own annual filings.
- [Healthcare](https://fullypowered.ai/industries/healthcare/), where facility licences, inspection certificates and registrations each renew on their own date.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where the register has grown over years and some of its owners have moved on.
- [Acquisitions and integration](https://fullypowered.ai/situations/acquisitions-and-integration/), where a newly acquired company's obligations join the register and need owners, verification and evidence before the first review.

Agreements with renewal and notice clauses belong in [contract renewal and notice register](https://fullypowered.ai/workflows/contract-renewal-notice-register/), which works under counsel's own counting rules. When an audit is coming, [audit preparation](https://fullypowered.ai/workflows/audit-preparation/) gathers the requests and evidence around it.

## What has to change for your company

Map your register's columns to the standard headers once, and keep your own words for each kind of obligation. Set the window and how often the review runs. Decide the scope for each reader. Name the reviewer, and who verifies each kind of obligation: usually counsel or the company secretary for company filings, and the environmental specialist for permit and monitoring duties. Set how often an entry must be verified again, keep the list of current owners up to date, and agree where evidence is kept so every reviewer can open it. Decide who updates the register after the review.

We sit with the person who keeps the register and the people who verify it, write down how the review is really done, and set it up in the AI product your company has approved: ChatGPT, Claude, Copilot or Gemini. It runs from files you supply and needs no connection to any registry or agency portal.

## What has been checked

Fully Powered AI wrote this workflow template from its own published map of the work. It was editorially reviewed on 11 November 2026. It was tried on its invented example in Claude on 11 November 2026, and the record of that run is published with the template. It has not yet been tested in a client environment, and it has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your organisation means running it on a past review your compliance lead remembers well, plus hard cases written in advance, each with its expected result: a report whose recorded date has passed with no evidence, a reminder that gives a different date from the register, a renewal with no due date and a frequency of every two years, an owner who has left, and a request to "just add a year". The reviewer checks every date against the register before anyone relies on the list. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

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

- [Contract renewal and notice register](https://fullypowered.ai/workflows/contract-renewal-notice-register/)
- [Audit preparation](https://fullypowered.ai/workflows/audit-preparation/)
- [Emissions activity data schedule](https://fullypowered.ai/workflows/emissions-activity-data-schedule/)

## Make it yours

This is the starting version. Fully Powered AI adapts workflow templates to how your company works, proves them on real work and rolls them out to the roles that use them. [Talk with us](https://fullypowered.ai/contact/).
