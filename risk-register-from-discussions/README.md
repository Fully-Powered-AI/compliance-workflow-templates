# Risk register from risk discussions

After a risk workshop or a leadership meeting, the risk lead gets a draft register of the risks people actually raised: the controls they said are in place, the mitigations they proposed and the questions still open, each traced to who said it and where. Ratings use your own scale, or none.

*Workflow template · Compliance, risk and privacy · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/risk-register-from-discussions/)*

## The outcome

The register catches up with the conversation. A good workshop surfaces more than anyone writes down, and the notes sit in a folder until the week before the board asks. This workflow template turns those notes into entries the same day, in the shape your register already uses, so the risk lead walks into the review with a draft instead of a blank sheet.

Every line can be checked. Each risk, each control and each proposed fix carries the name of the person who said it and the line of the notes where they said it. When two people disagree, about whether a supplier review still happens or how likely a failure is, both statements stay on the page with a question for the person who can settle it. Anything too vague to enter, or that has already happened, is listed with its reason instead of quietly dropped.

Ratings appear only on your organisation's own scale, and only where someone gave one or stated a figure that fits a level. Without your scale, nothing is rated. The AI assistant adds no risk nobody raised, proposes no fix of its own, names no owner and accepts nothing. The owner of each risk confirms the entry, and the leaders your organisation names decide what is treated, funded or accepted.

## Who starts the work, and when

The risk lead starts it: whoever keeps the company's risk register and runs its review, often the finance director, the operations director or the compliance lead. It runs after a risk workshop, before a quarterly or annual risk review, or after any leadership meeting where risks came up, in time for the risk lead to read the draft and send the questions before the register goes to leadership, the board or its risk committee.

## What they supply

- **The discussion records.** Workshop notes, meeting minutes or a transcript, with the date, who attended, and each point under the name of the person who made it.
- **The current risk register,** if you have one, as a spreadsheet export.
- **The incident log,** if you keep one, as an export.
- **Your rating scale,** if you have one: what each likelihood and impact level means, how they combine, and the rating at which a risk goes to named leaders.
- **A few settings:** the name of the review, the risk lead, and the meeting the draft is for.

## What comes out

One draft in a fixed order. Each entry gives the risk in the speakers' own words, who raised it and who else spoke to it, the existing controls with where the register says the evidence is kept, the proposed mitigations with any owner, date and cost that was mentioned, the owner of the risk if one was confirmed, the rating, and any linked incidents.

After the entries: what was raised but not entered and why, the register risks nobody discussed (left unchanged), incidents not linked to any entry, the numbered questions, each addressed to one person, and the risks whose rating meets your escalation rule, with the body that decides. The draft ends by saying that nothing has been added to the register, assigned, accepted or sent.

A good draft can be read against the notes line by line, and nobody finds their name against something they did not say.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), which keeps the register and the review it feeds.
- [Leadership](https://fullypowered.ai/functions/leadership/), where the risks that meet the escalation rule are treated, funded or accepted.
- [Operations and process improvement](https://fullypowered.ai/functions/operations-and-process-improvement/), where many of the risks live and most of the controls run.
- [Manufacturing](https://fullypowered.ai/industries/manufacturing/), where one supplier, one machine or one server can stop a line.
- [Software technology](https://fullypowered.ai/industries/software-technology/), where investors and enterprise buyers ask to see the register.
- [Professional services](https://fullypowered.ai/industries/professional-services/), where a few clients and a few senior people carry much of the business.
- [Nonprofits](https://fullypowered.ai/industries/nonprofits/), where trustees review the register and funders ask about it.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when the company's first real register has to come out of conversations held so far.
- [Private equity & portfolios](https://fullypowered.ai/situations/private-equity-and-portfolios/), where a portfolio company's board expects the register on a fixed rhythm.

## What has to change for your company

Supply your own rating scale, written in figures where you can: how often, how much, how long. Set the rating at which a risk goes to leaders and name who decides. Match the column headers to your register's export, or keep the defaults. Ask whoever takes notes to put a name against every point, because every entry is traced to one. Decide who answers questions about whether a law applies, since the draft never says. It runs in ChatGPT, Claude, Copilot or Gemini from the records you supply, with no connection to any system.

For the hazards of one task or one workplace, use [workplace risk assessment](https://fullypowered.ai/workflows/workplace-risk-assessment/). To test a plan before committing to it, use a [premortem before a decision](https://fullypowered.ai/workflows/premortem-before-a-decision/).

## What has been checked

FullyPowered AI wrote this workflow template. It was editorially reviewed on 11 November 2026. It was tried once on its invented example in Claude on 11 November 2026, and the record of that run is published with it. The run produced every part of the draft, but it was not blind: the example's published output had been read before the draft was written, so the close match between the two shows little. The run left several judgement calls open, such as whether a tender and losing half a customer's volume count as one event. The template has since been clarified on those points, with one sentence each, and has not been run again, so the published record is of the earlier wording. It has not yet been tested in a client environment. It has not yet been tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your environment means running it on the notes of a workshop your risk lead remembers well, plus hard cases written in advance, each with its expected behaviour: two people giving different ratings, a control one person says has lapsed, a remark too vague to enter, a renamed column in the register export, a line about one employee's health. The risk lead checks every entry against the notes before anyone relies on the draft. [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that test set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by FullyPowered AI.
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

- [Workplace risk assessment](https://fullypowered.ai/workflows/workplace-risk-assessment/)
- [Premortem before a decision](https://fullypowered.ai/workflows/premortem-before-a-decision/)
- [Decision log](https://fullypowered.ai/workflows/decision-log/)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/).
