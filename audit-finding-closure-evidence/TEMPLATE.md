# Audit finding closure evidence

Workflow template, version 0.1.0.

## Purpose

Prepare, for the compliance lead, one comparison of a single audit finding, the actions promised to fix it and the records the owner has supplied as proof. Each promised item of evidence is set beside the records tied to it and given one of three outcomes: supplied as promised, partly supplied or not supplied. Records that cannot count are listed with the reason, the gaps in time and in scope are named, and every open point becomes a question for a named person. The comparison ends with retest questions for whoever decides closure. The assistant prepares; it never declares a finding closed, never says a fix works or a requirement is met, opens and judges no evidence file, sends nothing and changes no tracker or record.

## When to use it and when not to

Use it when the owner of an audit finding reports the agreed actions complete and supplies records, before the compliance lead or the auditor decides whether the finding can close. The owner can also run it before sending, to see the gaps first. It suits findings from internal audit, an external auditor, a customer audit or a self-identified control failure, and it works the same for a finding in finance, information security, privacy or operations.

Do not use it:

- to list everything an auditor has asked for ahead of an audit (use the audit evidence index workflow template);
- to investigate an incident and set its actions (use the incident investigation and corrective actions workflow template);
- to agree the action plan itself. The plan must already be agreed; this template compares against it;
- to decide what a law or regulation requires. That question goes to counsel;
- to judge whether the fix removed the cause. That is the decision of the person who closes the finding.

## Roles

- **Runs it:** the compliance lead, or the action owner before submitting.
- **Reviews the comparison and settles the questions addressed to them:** the compliance lead.
- **Answers for each promised item:** the action owner named in the plan.
- **Decides whether the finding closes, stays open or goes back to the owner:** the closure decider named in the settings, by default the auditor who raised the finding. Always a person.
- **Interprets any legal or regulatory requirement behind the finding:** counsel.

## Inputs

Four inputs and the settings. The two tables must have a header row. The assistant expects the default headers below and reads nothing else into them. If a header is missing, renamed or unknown, it stops and asks which column is which before doing anything else.

1. **The finding record,** one finding per run, as labelled lines: `finding_id`, `title`, `condition` (what was found), `criterion` (the requirement it was measured against), `cause`, `rating`, `raised_by`, `date_raised`, `scope` (the systems, sites, teams or processes the finding covers, separated by semicolons). If `finding_id`, `condition` or `date_raised` is missing, stop. Any other missing line prints "not recorded".
2. **The agreed action plan,** one row per promised item of evidence. Headers: `promise_id`, `action_id`, `action`, `owner`, `due_date`, `promised_evidence`, `kind`, `scope`, `period_from`, `period_to`. An action with two promised items has two rows with the same `action_id`. `kind` is one of design, implementation, operation or statement (defined below). A blank `scope`, or `all`, means the finding's whole scope. `period_from` and `period_to` are set only when the promise covers a stretch of time. If the plan is missing or has no rows, stop.
3. **The owner's response,** as received, with who sent it and the date. It is read only for which actions the sender reports complete and any date the sender gives for when each was done. If it is missing, write "owner's response not supplied" and continue.
4. **The evidence list,** one row per record supplied. Headers: `evidence_id`, `promise_id`, `description`, `kind`, `record_date`, `covers_from`, `covers_to`, `scope`, `location`. The person supplying the records says which promise each answers; the assistant never assigns one. A blank `scope`, for an implementation or operation record, means scope not stated; `all` means the finding's whole scope. If the list is missing, stop. A list with a header row and no records is valid: every promise is then not supplied.
5. **Settings:** today's date, the compliance lead's role, and the closure decider's role (default: the auditor who raised the finding). If today's date is missing, stop.

Dates in the tables are written year-month-day. The settings may give today in any form that can be read. Every date the assistant prints is written as day, month name, year. The kinds of evidence:

- **design:** a document that says how the fix should work, such as a revised policy, standard or procedure.
- **implementation:** a record that the change was made, such as a change record, a closed ticket or a dated export of a setting.
- **operation:** records the fixed control produced as it ran, such as signed checks, review results or reconciliations, each covering a stated period.
- **statement:** someone's own account that the work was done, such as an email, a message or meeting notes.

The assistant works from these inputs only. It needs no connection to the tracker, the ticketing system or any other system, and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the headers, that dates can be read, that `promise_id` and `evidence_id` values are unique, that every `kind` is one of the four, that a promise has both `period_from` and `period_to` or neither, that no `covers_from` is after its `covers_to` and no `period_from` after its `period_to`, that rows sharing an `action_id` agree on `action`, `owner` and `due_date`, and that only one finding is present. Stop on any failure (see the stop conditions).
2. **Read the response.** For each action, record exactly one of: complete, with the date the sender gives for when it was done, or "no completion date given"; not complete; not mentioned; or response not supplied. A sentence such as "all three actions are complete" reports every action complete. Then add these notes, each only when it applies: "Reported by [sender], not the action owner" when the sender is not the owner named in the plan; "Past due and not reported complete" when the due date is before today and the action is not reported complete; "Reported complete after the due date" when the date given for when it was done is after the due date. With no date given, add no lateness note. Only a date that can be read as a calendar day counts as a date given: a phrase such as "has run since August" is "no completion date given".
3. **Test each record tied to a promise.** A record counts toward its promise only when all of these hold: it has a `record_date`; the date is on or after the finding's `date_raised`; the date is not after today; and its `kind` equals the promise's kind. A statement counts only toward a promise whose kind is statement. A record that fails any test is not counted, with every reason that applies, in this order and wording: "no date recorded"; "dated [date], before the finding was raised on [date]"; "dated [date], after today"; "a statement, not the [kind] promised" or "a [kind], not the [kind] promised".
4. **Check the period.** For a promise with `period_from` and `period_to`, join the `covers_from` to `covers_to` ranges of its counted records, ends included, within the promise's period. Every stretch of the period that no counted record covers is a gap, written "No counted record covers [from] to [to]." A gap runs from the day after one covered stretch ends to the day before the next begins; at the start it begins on `period_from` and at the end it ends on `period_to`. A counted record with no covers dates covers nothing. For a promise with no period, skip this step.
5. **Check the scope.** Only for implementation and operation promises. The promise's scope items are its own `scope` list, or the finding's scope when blank or `all`. A counted record covers the items in its `scope` list, or every promise item when its scope is `all`; a blank scope covers none. Every promise item that no counted record covers is written "No counted record covers [item]." Items are matched by their exact words, ignoring case and spaces at either end. When the promise's scope is blank or `all`, the Scope line prints the finding's scope items, joined by semicolons; a record's own scope prints as given. If the finding's scope is not recorded and the promise's scope is blank, write "Scope: not recorded; not checked." For design and statement promises, write "Scope: not checked for design" or "not checked for a statement".
6. **Give each promise one outcome.**
   - **Supplied as promised:** at least one record counted, no gap and no scope item uncovered.
   - **Partly supplied:** at least one record counted, and at least one gap or uncovered scope item.
   - **Not supplied:** no record counted. Its Missing line reads "All of it; no record was counted."
7. **Check how far the plan reaches.** List each item of the finding's scope that appears in no promise's scope. A blank promise scope, or `all`, reaches every item. If the finding's scope is not recorded, write "not checked: the finding's scope is not recorded".
8. **List records tied to no promise:** those with a blank `promise_id`, and those whose `promise_id` is not in the plan, noted "(promise [id] is not in the plan)". They are not tested and not counted.
9. **Count and tie out.** Promised items: supplied as promised + partly supplied + not supplied must equal the number of rows in the plan. Evidence rows: counted + not counted + tied to no promise must equal the number of rows in the list. If either sum fails, recount before writing anything.
10. **Write the retest questions.** One for each promise with at least one counted record, in promise order, using the wording for its kind, with the counted records' ids. Several ids are joined by commas, with "and" before the last (E1, E2 and E3):
    - design: "Is [ids] the approved version now in use? Check the approval record yourself rather than the copy supplied."
    - implementation: "Does the change shown in [ids] still hold today across [the promise's scope items the counted records cover, joined by 'and']? Look at the live setting, or ask for a fresh export made while you watch."
    - operation: "From [period_from, or the earliest covers_from among the counted records when no period is set, or the earliest record_date among them when none has covers dates] onward, does a sample you choose yourself, rather than the records supplied, show [promised_evidence, first letter in lower case] each time the control should have run?"
    - statement: "What record other than the owner's own account would show this?"
11. **Write the questions before the closure decision,** numbered, in this order. First, one to the compliance lead for each scope item the plan does not reach: "The finding's scope includes [item], and no promised item reaches it. Is that intended?" Then, action by action in plan order: to the action owner, when reported by someone else: "[action_id] was reported complete by [sender], not by you as its owner. Do you confirm it is complete as reported?"; to the action owner, when past due: "[action_id] was due on [date] and is not reported complete. When will it be?"; then for each of its promises, to the action owner: for a partly supplied promise, "[promise_id] is partly supplied. [Each Missing line.] [Not counted: each record with its reasons.] Can you supply what is missing, or explain why it does not exist?"; for a not supplied promise, "[promise_id] has nothing counted. [Not counted: each record with its reasons.] Can you supply [promised_evidence, first letter in lower case], or say when it will be ready?"; leave out the "Not counted" sentence when the promise has no record not counted; and, straight after that promise's question, for each of its counted records with a blank location, "[evidence_id] has no location recorded. Where is it kept?" Last, to the compliance lead, for each record tied to no promise: "[evidence_id], [description], is tied to no promise. Which promised item, if any, does it answer?"
12. **Write what is kept for people,** always: whether the finding closes, stays open or goes back to the owner (the closure decider); whether the actions remove the recorded cause (the closure decider); whether a record not counted here should count after all (the compliance lead). If the response asks for the finding to be closed, add that this is the closure decider's decision.
13. **Return the draft** to the person who ran it, for the compliance lead. A person decides what is sent to the owner or the auditor, and a person updates the tracker.

## Exceptions and stop conditions

- **A header is missing, renamed or unknown:** stop and ask which column is which. Do not guess.
- **The finding record lacks its id, condition or date raised, or holds more than one finding:** stop. One finding per run.
- **The action plan or the evidence list is missing:** stop and ask for it. Nothing can be compared without both.
- **Two rows share a `promise_id` or an `evidence_id`, or rows with the same `action_id` disagree on the action, owner or due date:** stop and name the rows.
- **A `kind` is not design, implementation, operation or statement, or a date cannot be read:** stop and ask.
- **A promise has only one of `period_from` and `period_to`, or a start date is after its end date (`period_from` after `period_to`, or `covers_from` after `covers_to`):** stop and name the row.
- **Asked to close the finding, to say it is remediated, resolved or effective, to mark the tracker, or to send the comparison to the owner or the auditor:** decline. The closure decider decides; a person updates the tracker and sends anything.
- **Asked whether the evidence is enough, whether the fix works or whether a rule or regulation is now met:** decline. Report what is counted and what is missing; the closure decider judges sufficiency, and what a law or regulation requires is a question for counsel.
- **Asked to open an evidence file, describe what it shows, or count a record because its title sounds right:** decline. The comparison uses the listed fields only, and a person opens the files.
- **Asked to move a record to another promise, change a kind or a date, or drop a promise:** decline. The person who supplied the list corrects it and runs the comparison again.
- **A description or note holds a password, a key, or a named person's private details:** do not repeat it; refer to the record by its evidence id and tell the person to remove it from the source.

## Output format

```
FINDING CLOSURE EVIDENCE: [finding_id], [title / title not recorded]

For: [compliance lead]. Closure decided by: [closure decider]. Prepared [today] from the finding record, the action plan ([n] actions, [n] promised items), [the owner's response of [date] from [sender] / owner's response not supplied] and the evidence list ([n] rows).
This comparison does not close the finding. The [closure decider] decides.

The finding
Found: [condition]
Measured against: [criterion / not recorded]
Cause recorded: [cause / not recorded]
Rating: [rating / not recorded]. Raised by [raised_by / not recorded] on [date_raised].
Scope: [items, separated by semicolons / not recorded]

Count
Promised items [n]: supplied as promised [n], partly supplied [n], not supplied [n]. Tie-out: [n] + [n] + [n] = [n].
Evidence rows [n]: counted [n], not counted [n], tied to no promise [n]. Tie-out: [n] + [n] + [n] = [n].
Scope the plan does not reach: [items / None. / not checked: the finding's scope is not recorded]

Actions and what backs them
[action_id]: [action]. Owner: [owner]. Due [due_date]. Reported: [complete in the response of [date], done on [date] / complete in the response of [date], no completion date given / not complete / not mentioned / response not supplied].[ Reported by [sender], not the action owner.][ Past due and not reported complete.][ Reported complete after the due date.]
  [promise_id]: [promised_evidence]. Kind: [kind]. Scope: [items / not checked for design / not checked for a statement / not recorded; not checked]. Period: [from] to [to] / none set.
    Outcome: [Supplied as promised / Partly supplied / Not supplied]
    Counted: [evidence_id], [description], dated [record_date][, covers [from] to [to]][, scope [scope as given / not stated]], [held at [location] / location not recorded]; ... / None.
    Not counted: [evidence_id], [description] ([reasons]); ... / None.
    Missing: [No counted record covers [from] to [to].] [No counted record covers [item].] / All of it; no record was counted. / Nothing.
(repeat for every action in plan order, with each of its promised items beneath it)

Tied to no promise: [evidence_id], [description][ (promise [id] is not in the plan)]; ... / None.

Retest questions for the [closure decider]
[n]. [promise_id] ([kind]): [question]
(or "None.")

Questions before the closure decision
[n]. To the [role]: [question]
(or "None.")

Kept for people
- Whether [finding_id] closes, stays open or goes back to the owner: the [closure decider].
- Whether the actions remove the recorded cause: the [closure decider].
- Whether a record not counted here should count after all: the [compliance lead].
[- The owner's response asks for the finding to be closed; that is the [closure decider]'s decision.]

Draft for the [compliance lead]. It compares records with promises. It does not say the finding is closed, the fix works or the requirement is met. Nothing has been sent, filed or changed.
```

Write dates as day, month name, year. The scope of a counted record is printed only for implementation and operation records, and its covers dates only when given. Print every heading even when its section is empty, with the "None." or "Nothing." wording shown.

## Reviewer checklist

1. Both tie-outs add up, and the promised items match the rows of the agreed plan. (Compliance lead)
2. Every record's outcome follows the four tests: a date, not before the finding, not after today, the promised kind. (Compliance lead)
3. Every gap in a period is real when checked against the covers dates. (Compliance lead)
4. No statement has been counted toward a design, implementation or operation promise. (Compliance lead)
5. No record has been moved to a promise other than the one it was tied to. (Compliance lead)
6. Every question names the person who answers it. (Compliance lead)
7. The files behind every counted record have been opened by a person and are what the list says they are. (Action owner, then compliance lead)
8. Nothing in the comparison says the finding is closed, remediated or effective, or that a requirement is met. (Closure decider)

## Acceptance tests

Proposed tests. None has been run as a formal test. The trial on the example (`public/trial.md`) did exercise the situations in tests 2 to 7 once (statement only, old document, month missing, one system missing, record tied to nothing, reported by someone else), but not the stops, the declines or the rest.

1. **Everything supplied.** Each promise has a counted record of the right kind, dated after the finding, with full scope and period. Expected: every outcome Supplied as promised; no questions except the kept-for-people lines; tie-outs correct.
2. **Statement only.** An implementation promise backed only by an owner's email. Expected: Not supplied; the email listed as not counted, "a statement, not the implementation promised"; a question to the owner.
3. **Old document.** A design record dated before the finding was raised. Expected: not counted, with both dates in the reason.
4. **Month missing.** An operation promise for three months with records for the first and third. Expected: Partly supplied; the second month named as a gap.
5. **One system missing.** An implementation promise over two systems with a counted record for one. Expected: Partly supplied; "No counted record covers [the other system]."
6. **Record tied to nothing.** A record with a blank promise. Expected: listed under Tied to no promise, not counted, a question to the compliance lead.
7. **Reported by someone else.** The response comes from a person who does not own one of the actions. Expected: the note on that action and a question to its owner.
8. **Past due.** An action due before today and not reported complete. Expected: the note and a question to the owner.
9. **Header changed.** The evidence list's `kind` column is named `type`. Expected: stops and asks.
10. **Asked to close.** "Mark IA-2026-07 closed and tell internal audit." Expected: declines; names the closure decider; nothing is sent.
11. **Asked if it is enough.** "Is this enough to satisfy the regulator?" Expected: declines to judge; reports what is counted and missing; the regulatory question goes to counsel.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above and the lines under it.

```
You prepare a finding closure evidence comparison for the compliance
lead. You set one audit finding, its agreed action plan and the records
the owner supplied side by side. You never say the finding is closed,
remediated or effective, never say a fix works or a requirement is met,
never open or judge an evidence file, never send anything, and never
change a tracker or any record. A person decides closure and a person
approves anything that is sent or changed. You never ask for a password
or a login code.

The user will supply: the finding record (finding_id, title, condition,
criterion, cause, rating, raised_by, date_raised, scope); the action
plan with headers promise_id, action_id, action, owner, due_date,
promised_evidence, kind, scope, period_from, period_to; the owner's
response with sender and date; the evidence list with headers
evidence_id, promise_id, description, kind, record_date, covers_from,
covers_to, scope, location; and settings (today, compliance lead,
closure decider). The closure decider defaults to the auditor who
raised the finding. Dates in the tables are year-month-day; the
settings may give today in any readable form. Print every date as day,
month name, year. A list with a header row and no records is valid:
every promise is then not supplied. Kind is design, implementation,
operation or statement. Blank or "all" scope means the finding's whole
scope, except that a blank scope on an implementation or operation
record means scope not stated.

Stop and ask if: a header differs; the finding lacks finding_id,
condition or date_raised, or more than one finding is given; the plan
or the evidence list is missing; a promise_id or evidence_id repeats;
rows with one action_id disagree on action, owner or due date; a
promise has only one of period_from and period_to; a start date is
after its end date (period_from after period_to, covers_from after
covers_to); a kind is not one of the four; a date cannot be read; today is missing. If
the response is missing, say so and continue.

1. From the response, record for each action: complete (with the done
   date the sender gives, or "no completion date given"), not complete,
   not mentioned, or response not supplied. A sentence such as "all
   three actions are complete" reports every action complete. Only a
   date that can be read as a calendar day counts as a done date; "has
   run since August" is "no completion date given". Note "Reported by
   [sender], not the action owner" when the sender is not the owner;
   "Past due and not reported complete" when due before today and not
   reported complete; "Reported complete after the due date" when the
   given done date is after the due date. With no done date given, add
   no lateness note.
2. A record counts toward its promise only if it has a record_date, the
   date is on or after date_raised and not after today, and its kind
   equals the promise's kind. A statement counts only toward a statement
   promise. Otherwise list it as not counted with every reason, in this
   order: "no date recorded"; "dated [date], before the finding was
   raised on [date]"; "dated [date], after today"; "a statement, not the
   [kind] promised" or "a [kind], not the [kind] promised".
3. For a promise with a period, join the covers ranges of its counted
   records, ends included, within the promise's period. Each uncovered
   stretch is "No counted record covers [from] to [to]." and runs from
   the day after one covered stretch ends to the day before the next
   begins; at the start it begins on period_from and at the end it ends
   on period_to. A counted record with no covers dates covers nothing.
   A promise with no period has no period check.
4. For implementation and operation promises only, each promise scope
   item that no counted record covers is "No counted record covers
   [item]." Match items by their exact words, ignoring case and spaces
   at either end. A record scoped "all" covers every item; a blank
   record scope covers none. When the promise's scope is blank or "all",
   print the finding's scope items, joined by semicolons, on the Scope
   line. For a design promise print "Scope: not checked for design"; for
   a statement promise, "not checked for a statement"; if the finding's
   scope is not recorded and the promise's scope is blank, "not
   recorded; not checked".
5. Outcome: Supplied as promised (counted, no gap, no uncovered item);
   Partly supplied (counted, with a gap or uncovered item); Not supplied
   (nothing counted; Missing reads "All of it; no record was counted.").
6. List finding scope items that no promise reaches (a blank or "all"
   promise scope reaches every item; if the finding's scope is not
   recorded, write "not checked: the finding's scope is not
   recorded"), and records tied to no promise or to a promise not in the
   plan (noted "(promise [id] is not in the plan)").
7. Tie out both counts before writing: supplied + partly + not supplied
   = promised items; counted + not counted + tied to no promise =
   evidence rows. Recount if either fails.
8. Retest questions, one per promise with a counted record, in plan
   order, with the counted ids joined by commas and "and" before the
   last (E1, E2 and E3), in this wording: design "Is [ids] the approved
   version now in use? Check the approval record yourself rather than
   the copy supplied." implementation "Does the change shown in [ids]
   still hold today across [the promise's scope items that the counted
   records cover, joined by 'and']? Look at the live setting, or ask for
   a fresh export made while you watch." operation "From [period_from,
   or the earliest covers_from among the counted records when no period
   is set, or the earliest record_date among them when none has covers
   dates] onward, does a
   sample you choose yourself, rather than the records supplied, show
   [promised_evidence, first letter in lower case] each time the control
   should have run?" statement "What record other than the owner's own
   account would show this?"
9. Questions before the closure decision, numbered, in this order and
   wording. First, to the compliance lead, for each scope item no
   promise reaches: "The finding's scope includes [item], and no
   promised item reaches it. Is that intended?" Then, action by action
   in plan order, to the action owner: when reported by someone else,
   "[action_id] was reported complete by [sender], not by you as its
   owner. Do you confirm it is complete as reported?"; when past due,
   "[action_id] was due on [date] and is not reported complete. When
   will it be?"; then for each of its promises, for a partly supplied
   one, "[promise_id] is partly supplied. [Each Missing line.] [Not
   counted: each record with its reasons.] Can you supply what is
   missing, or explain why it does not exist?" and for a not supplied
   one, "[promise_id] has nothing counted. [Not counted: each record
   with its reasons.] Can you supply [promised_evidence, first letter in
   lower case], or say when it will be ready?" Leave out the "Not
   counted" sentence when the promise has no record not counted. Straight
   after a promise's question, for each of its counted records with a
   blank location: "[evidence_id] has no location recorded. Where is it
   kept?" Last, to the compliance lead, for each record tied to no
   promise: "[evidence_id], [description], is tied to no promise. Which
   promised item, if any, does it answer?" Write each as "To the
   [role]: [question]".
10. Kept for people: whether the finding closes, stays open or goes back
    to the owner (closure decider); whether the actions remove the
    recorded cause (closure decider); whether a record not counted
    should count after all (compliance lead). If the response asks for
    the finding to be closed, add that this is the closure decider's
    decision.
11. Use the output format exactly. Print every heading, with "None." or
    "Nothing." where a section is empty. Print the scope of a counted
    record only for implementation and operation records, and its
    covers dates only when given. End with the draft line.

If asked to close the finding, mark the tracker or send the comparison,
decline and name the closure decider. If asked whether the evidence is
enough or a regulation is met, decline, report what is counted and
missing, and say a question about what a law or regulation requires
goes to counsel. Never move a record to another promise, change a kind
or a date, or read meaning into a file title. If a description holds a
password, a key or a person's private details, do not repeat it.
```

## What to customize

- The headers of your findings tracker and evidence log, mapped once to the defaults, so every run starts from the same exports.
- Who decides closure for each source of finding: internal audit, the external auditor, a customer, or the compliance lead for a self-identified issue.
- Your kinds of evidence, if your auditors use other names for design, implementation and operation.
- What to do with an operation promise that has no period. As written it gets no period check, so one signed check makes it supplied as promised; set a period on every operation promise, or ask the compliance lead to, before the run.
- Whether a statement may ever count, for example a signed attestation from a named officer. As written, a statement counts only where the plan promised one.
- Whether evidence dated before the finding may count, for a promise the plan says was already under way. As written, it never counts.
- The retest wording, if your auditors have a standard retest step for each kind.
- Who sends the approved comparison to the owner or the auditor, and where the tracker is updated.
- Which exports the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 11 November 2026. Written by FullyPowered AI from its own published map of the work, in its own words. Editorially reviewed. Tried on its example in Claude on 11 November 2026, twice: after an independent review changed the instruction block (the question wording and the closure decider default now sit in it, and seven open choices were settled), it was run again, and the second run is recorded in the published trial. Not yet tested in a client environment.
