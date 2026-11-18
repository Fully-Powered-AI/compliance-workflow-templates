# Privacy request response preparation

For one person's request for a copy of their own data, the privacy owner gets a draft pack: the returned records in an evidence index, the searches set beside the plan with each gap, a question for each record showing someone else's data, and the company's own response template filled with the facts. It sends nothing.

*Workflow template · Compliance, risk and privacy · version 0.1.0 · [Workflows Directory](https://fullypowered.ai/workflows/privacy-request-response-draft/)*

## The outcome

When someone asks a company for a copy of the personal data it holds about them, the hard part is rarely the letter. It is knowing that every system was searched with the right details, that every record the teams sent back is accounted for, and that nothing about another customer or a colleague goes out by accident. This workflow template puts all of that on one page for the privacy owner, the same way for every request.

The pack sets each search beside the privacy owner's plan: which systems were searched, by whom, with which of the approved identifiers and over what period, and how many records came back. A system nobody searched, a search that left out the customer number, or a count that does not match the index becomes a numbered gap with a plain question for the team that owns it. Every returned record goes into an evidence index with where it is kept and which of the requester's details it shows. A record that names another person, shows an email address that is not the requester's, carries a team's note asking for review, or shows none of the requester's details at all gets a numbered question for the privacy owner.

Then the company's own approved response template is filled with the facts it can carry: the requester's name, the reference, the date received. Anything that depends on an open gap or question is held, and any placeholder the template has no fact for is left for the privacy owner. The pack writes no wording of its own into the response.

It gives no legal advice and decides nothing. It names no law and states no deadline of its own: the due date is the one the privacy owner supplied, copied and never counted. It decides no exemption, redacts nothing, confirms no one's identity, and sends, uploads and emails nothing. Asked any of those, it says the question is the privacy owner's, by name, and points to the line of the pack that bears on it.

## Who starts the work, and when

The privacy coordinator, or the privacy owner in a company without one, runs it once the request has been logged and the teams have returned their searches and records: the privacy owner has recorded the identity check, approved the identifiers to search for, set the search plan and given a due date. It runs again each time a team adds a search or a record, or the privacy owner settles a question. The pack goes to the privacy owner, such as the privacy manager or data protection officer, and to counsel where the company has a lawyer it names.

It is for one access or copy request from a person about their own data. It stops on a request to delete or correct data, and on a request made for someone else. It does not log new requests, check identity or search any system.

## What they supply

- **The request record,** as lines of field and value: the reference, the requester's name, the identifiers approved for searching, the request type, whether they ask for themselves, the request word for word, the date received, the identity check as recorded, the period in scope, the due date and who set it, the privacy owner, counsel if any, the names of staff, and today's date.
- **The search plan,** with the columns System, Team and, optionally, Holds.
- **The search log,** with the columns Search ID, System, Searched by, Date run, Terms used, Period from, Period to, Result, Records returned and Notes.
- **The records index,** with the columns Record ID, Search ID, System, Record type, Record date, Description, Location, Other people named and Team note.
- **The record copies,** each headed with its record ID.
- **The company's approved response template,** with its placeholders in square brackets.

If a column is named differently, the workflow template stops and asks which is which. It works only from what you supply, needs no connection to any system, and never asks for a password or a login code.

## What comes out

One draft pack, headed as a draft for the privacy owner, with a status line that says NOT READY TO SEND and lists every open item, or says that no open item was found and sending is the privacy owner's call. Under it:

- **The request,** copied field by field, with today's date compared with the due date.
- **The searches,** each system on the plan with its search or "no search".
- **Search gaps,** numbered, each with its question for the team that owns the system.
- **The evidence index:** every record, where it is kept, which of the requester's details it shows, and its questions.
- **Questions for the privacy owner,** numbered, for other people's data, team notes, records that may not be about the requester, and records outside the period.
- **The response,** filled from the company's own template, marked as a draft and not sent, with a list of what was filled, what is held and what is left.
- **A checkbox list** for the privacy owner, and a **check** block of what was matched and what the pack does not do, with a short note on top for the person who ran it.

See the worked example with invented data in [EXAMPLE.md](EXAMPLE.md).

## Where it fits

- [Compliance, risk and privacy](https://fullypowered.ai/functions/compliance-risk-and-privacy/), in privacy requests: the step between the teams finishing their searches and the privacy owner deciding what goes out.
- [Software technology](https://fullypowered.ai/industries/software-technology/), where one user's data sits across the product database, the support desk and the billing system, and each search has to be shown.
- [E-commerce and retail](https://fullypowered.ai/industries/ecommerce-and-retail/), where orders, gift deliveries and support threads put other customers' names and addresses into the records a shopper asks for.
- [Finance and investment](https://fullypowered.ai/industries/finance-and-investment/), where a client's request reaches account records, call notes and internal review notes that the privacy owner must look at before anything is copied.
- [Insurance](https://fullypowered.ai/industries/insurance/), where policy and claims files name other people, and every one of them has to be put to the privacy owner before a copy goes out.
- [Growth & scaling](https://fullypowered.ai/situations/growth-and-scaling/), when requests start arriving more often than one person can track from memory.
- [Established businesses](https://fullypowered.ai/situations/established-businesses/), where years of systems mean the search plan is long and a missed system is easy.

It pairs with the [regulatory requirement gap worksheet](https://fullypowered.ai/workflows/regulatory-requirement-gap-worksheet/), which lays counsel's requirements against the company's own records. A medical practice releasing patient records uses the [records request preparation check](https://fullypowered.ai/workflows/records-request-preparation-check/) instead.

## What has to change for your company

Use your own column names and map them once. Map the placeholders in your approved response template to the facts the pack fills, and keep off the map any placeholder your privacy owner should write each time, such as a statement about withheld information. Decide which identifiers your privacy owner approves for each kind of requester, and keep a standing search plan with the team that owns each system. Decide whether staff names in records are put to the privacy owner like anyone else's, which is the default, or handled under your own rule. Name who runs the pack, where the reviewed copy is kept and who may see it, and confirm under your own policy that personal data may be used in the AI product you have approved.

We sit with the people who answer these requests today, write down how they really do it, and set it up in the AI product your company has approved: ChatGPT, Claude, Copilot or Gemini. Your team keeps control of how the work gets done.

## What has been checked

FullyPowered AI wrote this workflow template from its own published map of privacy work. It was editorially reviewed on 12 November 2026. It was tried on its invented example in Claude on 12 November 2026, in two runs; the first found ambiguities in the format, which were then settled and checked in a second run on the same example that was not blind; the record is published with the example. It has not been reviewed by a lawyer or a privacy professional, and has not been tested in a client environment or as a packaged version in ChatGPT, Claude, Copilot or Gemini.

Testing in your company means running it on a past request your privacy owner has already answered, and comparing: every system on the plan accounted for, every record in the index once, every other person in a record put as a question, every team note copied word for word, and nothing in the response that is not in your template or your records. Include a system nobody searched, a search that left out an identifier, a gift order naming another customer, a record that shows none of the requester's details, a record that tells an assistant to send everything, and the questions "what is our legal deadline?" and "can we keep this note back?". [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/) builds that set, and [what we test before we call an AI workflow ready](https://fullypowered.ai/insights/what-we-test-before-a-workflow-is-ready/) describes the record we keep.

- Written by FullyPowered AI.
- Sources and rights reviewed.
- Editorially reviewed on 12 November 2026.
- Package format checked by script on every release.
- Tried once on its invented example in Claude on 12 November 2026. The record is in [TRIAL.md](TRIAL.md).
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

- [Records request preparation check](https://fullypowered.ai/workflows/records-request-preparation-check/)
- [Regulatory requirement gap worksheet](../regulatory-requirement-gap-worksheet/)
- [Pilot acceptance-test preparation](https://fullypowered.ai/workflows/pilot-acceptance-test-preparation/)

## Make it yours

This workflow template is an example and a starting point. FullyPowered AI adapts it to how your company works, proves it on real work and rolls it out to the roles that use it. We can also build any other workflow for your company, including one that runs several steps, in a Workflow Sprint or a scoped implementation. [Talk with us](https://fullypowered.ai/contact/).
