# Audit finding closure evidence: trial on the example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (claude-sonnet-5-5)
- **Date:** 2026-11-11

This records two runs of the workflow template on its example, both on 11 November 2026. The first run is recorded below as it was; what was changed after it, and the second run, follow it. The inputs are the sample ones; no client data was used. The model that ran it did not write the template.

## Inputs used

The five inputs in `public/example.md` under "The inputs": the settings (today 4 November 2026), the finding record IA-2026-07, the four-row action plan, the owner's response of 2 November 2026 and the eight-row evidence list. They were taken as written, with nothing added. The example's own comparison was not read until the output below was finished.

## First run: what came out

The model followed the instruction block and the output format in the template. Every heading was printed. The output is shown here in full.

```
FINDING CLOSURE EVIDENCE: IA-2026-07, Leavers keep access to the payments admin console

For: Compliance lead. Closure decided by: Head of internal audit. Prepared 4 November 2026 from the finding record, the action plan (3 actions, 4 promised items), the owner's response of 2 November 2026 from IT operations manager and the evidence list (8 rows).
This comparison does not close the finding. The Head of internal audit decides.

The finding
Found: In a sample of 25 people who left between 1 January and 31 March 2026, 4 still had active accounts on the payments admin console or the customer support tool between 6 and 19 working days after their last day.
Measured against: Access control standard AC-02, revision 3, section 4: access to production systems is removed by the end of the next working day after a person's last day.
Cause recorded: Leaver notices reach IT in a weekly email from the people team rather than on the leaving date, and the payments admin console and the customer support tool have their own logins outside single sign-on.
Rating: High. Raised by Internal audit on 14 April 2026.
Scope: Payments admin console; Customer support tool

Count
Promised items 4: supplied as promised 2, partly supplied 2, not supplied 0. Tie-out: 2 + 2 + 0 = 4.
Evidence rows 8: counted 5, not counted 2, tied to no promise 1. Tie-out: 5 + 2 + 1 = 8.
Scope the plan does not reach: None.

Actions and what backs them
A1: Send leaver notices from the HR system to the IT service desk automatically on the leaving date. Owner: People operations lead. Due 30 June 2026. Reported: complete in the response of 2 November 2026, done on 22 June 2026. Reported by IT operations manager, not the action owner.
  P1: Service desk record showing the automatic leaver notice switched on. Kind: implementation. Scope: Payments admin console; Customer support tool. Period: none set.
    Outcome: Supplied as promised
    Counted: E1, Service desk ticket 4471: automatic leaver notice from the HR system switched on, dated 22 June 2026, scope all, held at Service desk / ticket 4471.
    Not counted: None.
    Missing: Nothing.
A2: Put the payments admin console and the customer support tool behind single sign-on. Owner: IT operations manager. Due 31 July 2026. Reported: complete in the response of 2 November 2026, done on 28 July 2026.
  P2: Change record for each system moved to single sign-on. Kind: implementation. Scope: Payments admin console; Customer support tool. Period: none set.
    Outcome: Partly supplied
    Counted: E2, Change record CHG-0912: payments admin console moved to single sign-on, dated 28 July 2026, scope Payments admin console, held at Change log / CHG-0912.
    Not counted: E6, Email from the IT operations manager saying the customer support tool moved to single sign-on (a statement, not the implementation promised).
    Missing: No counted record covers Customer support tool.
A3: Add a monthly leaver access check for both systems to the access control standard and run it. Owner: IT operations manager. Due 31 August 2026. Reported: complete in the response of 2 November 2026, no completion date given.
  P3: Access control standard with the monthly leaver check added. Kind: design. Scope: not checked for design. Period: none set.
    Outcome: Supplied as promised
    Counted: E3, Access control standard AC-02 revision 4 with section 6 monthly leaver check, dated 3 August 2026, held at Policy library / AC-02.
    Not counted: E7, Access control standard AC-02 revision 3 (dated 15 January 2026, before the finding was raised on 14 April 2026).
    Missing: Nothing.
  P4: Signed monthly leaver access checks for both systems. Kind: operation. Scope: Payments admin console; Customer support tool. Period: 1 August 2026 to 31 October 2026.
    Outcome: Partly supplied
    Counted: E4, Monthly leaver access check for August 2026 signed by the IT operations manager, dated 2 September 2026, covers 1 August 2026 to 31 August 2026, scope Payments admin console; Customer support tool, held at IT share / Access checks / 2026; E5, Monthly leaver access check for October 2026 signed by the IT operations manager, dated 2 November 2026, covers 1 October 2026 to 31 October 2026, scope Payments admin console; Customer support tool, location not recorded.
    Not counted: None.
    Missing: No counted record covers 1 September 2026 to 30 September 2026.

Tied to no promise: E8, Screenshot of the single sign-on user list for the payments admin console.

Retest questions for the Head of internal audit
1. P1 (implementation): Does the change shown in E1 still hold today across Payments admin console and Customer support tool? Look at the live setting, or ask for a fresh export made while you watch.
2. P2 (implementation): Does the change shown in E2 still hold today across Payments admin console? Look at the live setting, or ask for a fresh export made while you watch.
3. P3 (design): Is E3 the approved version now in use? Check the approval record yourself rather than the copy supplied.
4. P4 (operation): From 1 August 2026 onward, does a sample you choose yourself, rather than the records supplied, show signed monthly leaver access checks for both systems each time the control should have run?

Questions before the closure decision
1. To the People operations lead: A1 was reported complete by IT operations manager, not by you as its owner. Do you confirm it is complete as reported?
2. To the IT operations manager: P2 is partly supplied. No counted record covers Customer support tool. Not counted: E6 (a statement, not the implementation promised). Can you supply what is missing, or explain why it does not exist?
3. To the IT operations manager: P4 is partly supplied. No counted record covers 1 September 2026 to 30 September 2026. Can you supply what is missing, or explain why it does not exist?
4. To the IT operations manager: E5 has no location recorded. Where is it kept?
5. To the Compliance lead: E8, Screenshot of the single sign-on user list for the payments admin console, is tied to no promise. Which promised item, if any, does it answer?

Kept for people
- Whether IA-2026-07 closes, stays open or goes back to the owner: the Head of internal audit.
- Whether the actions remove the recorded cause: the Head of internal audit.
- Whether a record not counted here should count after all: the Compliance lead.
- The owner's response asks for the finding to be closed; that is the Head of internal audit's decision.

Draft for the Compliance lead. It compares records with promises. It does not say the finding is closed, the fix works or the requirement is met. Nothing has been sent, filed or changed.
```

## First run: what was observed

**Every required part was produced.** All headings, both tie-outs, the four retest questions, the five questions before the decision and the kept-for-people lines. No stop condition was met, so nothing needed asking.

**Comparison with the published example.** The output matches the published comparison line for line. The model found no difference in outcomes, counts, wording or order. Checked against the reviewer checklist: both tie-outs add up (2 + 2 + 0 = 4 and 5 + 2 + 1 = 8), the statement E6 was not counted toward an implementation promise, the September gap is real, no record was moved to another promise, every question names who answers it, and nothing says the finding is closed or the fix works. Checklist item 7 (a person opens the files) cannot be checked by the assistant and was not.

**Facts not in the inputs.** None in either output. Counts, "3 actions" and the day-level gap dates are derived from the inputs.

**Places the instructions left a choice.** The model made the choices below, and the match with the example may be partly luck.

- A3 was reported as "has run since August", which is not a date. The model treated it as "no completion date given". The template does not say what to do with a vague date like this.
- The template does not say how to write the edges of a gap. The model took the day after one range ends to the day before the next begins (1 to 30 September). Another reader could write it differently.
- For a partly supplied promise with nothing under Not counted (P4), the question wording has a "[Not counted: ...]" slot with nothing to put in it. The model left it out. The template does not say to.
- Where a promise has both a partly-supplied question and a counted record with no location, the template does not fix which question comes first. The model put the promise question first.
- P1's scope in the plan is "all". The template leaves it open whether the scope line prints "all" or the named items it stands for. The model printed the items.
- When more than one record is counted for a design promise, the template does not say how several ids are joined in the question. Not needed here.
- The header says "the owner's response" even when the sender owns only some of the actions, as here.
- Dates in the tables are year-month-day, but the settings in the example give today as "4 November 2026". It was read without trouble, yet the template does not say which form settings take.

**A gap in the paste-in block (found in the first run; fixed afterwards, see below).** The fenced instruction block says "Use the question wording in the template", but only the block and the output format are pasted. The exact wording of the questions before the decision, and the "Scope: not checked for design" lines, are in the procedure and not in the block. In this trial the whole template was in view, so this was not tested. A user who pastes only the block would have to guess that wording. The block also leaves out the default closure decider.

**What this trial does not show.** It is one run on one example, by one model. It did not test the stop conditions, the declines, a missing response, a future-dated period or the other ten acceptance tests. It shows that the instructions can be followed to the published result, not that they hold on real findings.

## Changed after the first run

An independent review of the first run found that a user who pastes only the instruction block and the output format could not reproduce the example. Afterwards:

- The block now carries the exact wording of every question before the closure decision, the default closure decider (the auditor who raised the finding), the "Scope: not checked for design" lines and the rules under the output format (dates as day, month name, year; a counted record's scope only for implementation and operation records; covers dates only when given). The pasting line now says the block is followed by the output format and the lines under it.
- The block now also states that an evidence list with a header row and no records is valid, that "all three actions are complete" reports every action, that no lateness note is added when no done date is given, that the period join stays within the promise's period, and that items are matched ignoring case and spaces at either end (the procedure and the block now say the same).
- Seven choices the first run found open were settled in one sentence each: a vague done date such as "has run since August" is "no completion date given"; a gap runs from the day after one covered stretch ends to the day before the next begins (or from the start or to the end of the period); the "Not counted" sentence is left out of a question when the promise has none; a promise's question comes before the no-location questions for its records; a promise scope of "all" or blank prints the finding's scope items; several ids are joined by commas with "and" before the last; the settings may give today in any readable form and every printed date is day, month name, year.
- The example's inputs and comparison did not change.

## Second run

The template was run again on the same sample inputs, by Claude Sonnet 5.5 (claude-sonnet-5-5), in Claude Code, on 11 November 2026, working only from the changed instruction block, the output format and the lines under it. The model that edited the template also made this run, and it had read the published comparison while editing, so this run is weaker evidence than the first; it was not a fresh reader.

What was observed:

- The output matched the published comparison line for line: the same outcomes, counts, tie-outs, gap, questions and wording. The A3 done date came out as "no completion date given", the gap as 1 September 2026 to 30 September 2026, P1's scope line as both named systems, P4's question without a "Not counted" sentence followed by the E5 location question, and every date as day, month name, year.
- Nothing in the run needed wording that is outside the pasted text. Each of the seven choices listed above was answered by a sentence in the block, where the first run had to guess.
- A real test of the paste-only case needs a reader who has seen neither the template nor the example. That has not been done.
- After this run, small additions were made to the template for a later review: a stop when a promise has only one period date or a start date is after its end date, and a fallback for the operation retest question when no period is set. They do not apply to the example's inputs, so the example and this record were not changed and the template was not run again for them.
- The limits in the first run's last paragraph still apply: one example, no stop conditions, declines or other acceptance tests were exercised.
