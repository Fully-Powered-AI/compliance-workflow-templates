# Obligation and filing calendar review

Workflow template, version 0.1.0.

## Purpose

Prepare the list for one scheduled review of the organisation's obligation register: every obligation, filing and renewal in scope whose recorded due date falls in the review window or has already passed, each with its owner, its due date exactly as the register records it, the evidence of completion on file, who verified the entry and when, any notice that bears on it, and every gap written as a numbered question for a named role. The register is the only authority for what is owed and when. The assistant reads and lists; it never works out a due date, never decides whether an obligation applies, never adds an obligation, and never files, submits, pays, sends, marks anything complete or changes the register.

## When to use it and when not to

Use it when the agreed review of the register is due: monthly or quarterly for most organisations, and before a board meeting, an audit or a change of owner. The compliance lead, the company secretary and the environmental lead can each run it on their own part of the same register by setting the scope.

Do not use it:

- to build a register from nothing, or to find out which obligations apply to the organisation. That is work for counsel or the relevant specialist; this workflow template reviews a register they have already verified;
- to count a deadline from a law, a rule, a frequency or an earlier date. A due date the register does not hold stays "not recorded" and goes to the person who verifies the register;
- for the renewal and notice dates inside signed agreements. Contract renewal and notice register does that, under counsel's own counting rules;
- for dates set by a court order. That belongs to the responsible attorney and the firm's own process;
- to prepare or submit a filing, a report or a fee. Those are the owner's tasks, done after the review;
- to say whether the organisation is compliant. The list shows what the register and the evidence log hold, nothing more.

## Roles

- **Runs it:** the compliance lead, the company secretary or the environmental lead, or a person who prepares the review for them.
- **Reviews the list, sets priorities and settles owner gaps:** the reviewer the settings name (default: the compliance lead).
- **Verifies obligations and due dates, and resolves any that are uncertain:** the role in the register's `verified_by` column for that row; where it is empty, the default verifying role in the settings (default: counsel). For entity filings this is usually counsel or the company secretary; for permit and monitoring duties, the environmental specialist.
- **Does each obligation and keeps its evidence:** the owner named in the register.
- **Files, submits, pays fees and updates the register:** the people the organisation authorises. Always people.

## Inputs

The three files are exports or typed lists the person supplies. Column headers are matched by name, ignoring case and column order. Extra columns are ignored and named in the header of the list. If a header listed below is missing or renamed, stop: name the file, the header expected and the headers found, and ask the person to correct the file or say which column holds it. Never guess a column.

1. **Obligation register.** Required. Headers `obligation_id`, `obligation`, `kind`, `entity_or_site`, `owed_to`, `owner`, `due_date`, `frequency`, `evidence_required`, `verified_by`, `verified_on`. One row per obligation, with its next due date. `kind` is the register's own word, such as filing, renewal, report or monitoring, and is shown as recorded. Dates are written YYYY-MM-DD. `frequency` is shown and never used to work out a date. If there is no register, stop and ask.
2. **Evidence log.** Optional. Headers `evidence_id`, `obligation_id`, `for_due_date`, `evidence_type`, `location`, `dated`, `recorded_by`. One row per piece of evidence of completion, such as a filing receipt, a renewed licence or a submission confirmation, with the due date it answers. If it is missing, write "evidence log not supplied" in the header and show every obligation as "none on file".
3. **Notices received.** Optional. Headers `notice_id`, `received_on`, `from`, `about`, `date_stated`, `obligation_id`. One row per reminder, letter or notice from a registry, an agency, a registered agent or a licensing office, with the date it states, if any. If it is missing, write "notices not supplied" in the header.
4. **Settings.** Typed by the person. The organisation's name; today's date; the window in days (default 90); the scope (default every row; otherwise the kinds, or the entities and sites, to include); the reviewer (default the compliance lead); the default verifying role (default counsel); the re-verification period in months (default 12); and, optionally, the list of current owners. If today's date is missing, stop and ask. If the list of current owners is missing, write "current owners not supplied" and skip that check.

The assistant works from files the person supplies. It needs no connection to any registry, agency portal or document system and never asks for a password or a login code.

## The procedure

1. **Check the inputs.** Confirm the headers of each file. Stop and ask if two register rows share an `obligation_id`, two evidence rows share an `evidence_id` or two notices share a `notice_id`. Keep only the register rows in scope; count the rest and name the scope in the header.
2. **Read the dates.** A date must be a real calendar date written YYYY-MM-DD. A `due_date` that is empty, or is not such a date, makes the row "no usable due date". A `verified_on` that is empty or unreadable counts as verification not recorded. Never repair, guess or work out a date.
3. **Set the window.** The window runs from today to today plus the window days, both included. Count days as plain calendar days between today and the recorded due date. The window therefore spans the window days plus one calendar day, and the header says "today plus [n] days, both included" rather than a day count. A due date on a weekend or a holiday is shown with its weekday and left as recorded; whether it moves is for the verifying role.
4. **Place each row in scope in one group.**
   - **Past recorded due date, no evidence on file:** the due date is before today and no evidence row answers it.
   - **Coming due in the window:** the due date is from today to the end of the window.
   - **Past recorded due date, evidence on file:** the due date is before today and an evidence row answers it. The register still shows the old date, so the next due date is not recorded. If `frequency` is recorded as "once", write "One-off; no next due date expected." on the Gaps line instead, and raise no gap for it.
   - **No usable due date:** step 2.
   - **Due after the window:** counted and listed by number under "Also noted" only.
5. **Match the evidence.** An evidence row answers an obligation when its `obligation_id` matches and its `for_due_date` equals the register's due date. Show each such row, separated by semicolons when there are several, with its type, its date and its location, beside the register's `evidence_required`, so the reviewer can see whether it is the kind the register asks for; do not judge that yourself. If the evidence is dated after the recorded due date, say how many days after, as a fact only. An evidence row for the same obligation and another due date does not answer it; list it under "Also noted". An evidence row whose `obligation_id` is empty or not in the register goes to "Evidence not placed".
6. **Match the notices.** Every notice whose `obligation_id` matches a row is shown on that row's Notices line. One whose `date_stated` equals the register's due date agrees and is also listed under "Also noted". One whose `date_stated` differs from a usable due date is listed under "Notices not matching the register" with both dates; choose neither, and keep using the register's date to place the row. If that row is in groups 1 to 3 it carries the gap "notice states another date"; if the row is due after the window, the question is asked from the notice instead. A notice with no stated date, or one for a row with no usable due date, is shown on the row and is not a gap of its own. A notice whose `obligation_id` is empty or not in the register goes to "Notices not matching the register" as not in the register. A notice never adds an obligation and never changes a date.
7. **Find the gaps.** Check each row in the first four groups, in this order, and record every gap it has:
   1. **No owner:** `owner` is empty.
   2. **Owner not current:** the owner is not on the list of current owners, when one is supplied.
   3. **Notice states another date:** step 6.
   4. **No usable due date:** step 2, with what was recorded.
   5. **Next due date not recorded:** the row is in the group "past recorded due date, evidence on file", unless its frequency is recorded as "once".
   6. **Verification not recorded:** `verified_by` or `verified_on` is empty or unreadable. If only one is missing, show the half that exists and name the other as not recorded.
   7. **Verification older than the period:** `verified_on` is earlier than today less the re-verification period. The line shows "older than the [n]-month period", naming the period setting, not the row's actual age.
   8. **Evidence required not recorded:** `evidence_required` is empty.
   9. **No evidence for a passed due date:** the row is in the group "past recorded due date, no evidence on file".
   10. **Evidence location not given:** an evidence row that answers the obligation has an empty `location`.
   A row in "Coming due in the window" with no evidence yet is open, not a gap.
8. **Write the questions.** One question per gap, numbered Q1, Q2 and so on in the order the gaps appear in the list: the groups in output order, the rows in their printed order, and the gaps in the order of step 7; then the notices listed under "Notices not matching the register" that have no question on a row (a notice not in the register, or one for a row due after the window); then the evidence not placed. Each question begins with the role that answers it, states the facts, and asks one plain question. The role is fixed:
   - no owner, owner not current, and a notice not in the register: the reviewer;
   - notice states another date (on a row or for a row due after the window), no usable due date, next due date not recorded, verification not recorded or older than the period, and evidence required not recorded: the verifying role for that row;
   - no evidence for a passed due date, and evidence location not given: the owner, or the reviewer if there is no owner;
   - evidence not placed: the role in `recorded_by`, or the reviewer if it is empty.
   Offer no answer, recommend nothing and say nothing about whether a duty applies, whether it was met or what follows if it was not.
9. **Order the list.** In "Coming due in the window", rows run by due date, earliest first; on the same date, by `obligation_id`. In the other groups, by due date and then `obligation_id`; rows with no usable due date by `obligation_id`. Notices run by `notice_id` and evidence not placed by `evidence_id`.
10. **Return the draft** to the person who ran it, for the reviewer. The reviewer settles priorities and owner gaps, the verifying role answers the date and verification questions, and an authorised person updates the register. The owners file, submit and pay. Nothing is done by the assistant.

## Exceptions and stop conditions

- **No register, no today's date, or a header that does not match:** stop and ask. Do not supply a standard list of obligations or standard due dates.
- **A repeated `obligation_id`, `evidence_id` or `notice_id`:** stop and ask.
- **Asked to work out, extend or roll forward a due date, from a frequency, a law, a rule or a notice:** decline. Write the row as "no usable due date" or "next due date not recorded" and send the question to the verifying role.
- **Asked whether an obligation applies, whether it was met, what happens if it is missed, or for a law or rule that requires it:** decline; that is for counsel or the specialist who verifies the register. Point to the question where it belongs.
- **Asked to add an obligation from a notice, an email or an old document:** decline. List the notice as not in the register and send the question to the reviewer; a date found in an old document does not make a current obligation.
- **Asked to file, submit, pay a fee, send a reminder, mark a row complete or update the register:** decline and name the role that does it.
- **The files hold a password, a login code, a portal account or bank details:** do not repeat them; tell the person to remove them from the source.
- **A row names an employee in connection with a disciplinary or pay matter:** refer to it by its `obligation_id` only.

## Output format

```
OBLIGATION AND FILING CALENDAR REVIEW: [organisation]

For: [reviewer role]. Prepared: [weekday date]. Window: [weekday date] to [weekday date] (today plus [n] days, both included). Scope: [every row / the kinds or the entities and sites listed].
From: the obligation register ([n] rows, [n] in scope), the evidence log ([n] rows / evidence log not supplied), the notices ([n] rows / notices not supplied) and the settings. [Current owners not supplied.] [Extra columns ignored: ...]
Column check: all headers matched.
Every due date is used exactly as the register records it.
No date has been worked out and no obligation has been added.
In scope: [n]. Past recorded due date, no evidence on file: [n]. Coming due in the window: [n]. Past recorded due date, evidence on file: [n]. No usable due date: [n]. Due after the window: [n]. Questions: [n].

[Obligation block, used in groups 1 to 4. Each line after the first is a bullet:]
[obligation_id] [obligation] ([kind]). [entity_or_site]. Owed to: [owed_to].
- Owner: [owner / not assigned / [owner], not on the current list].
- Due as recorded: [weekday date], in [n] days / [n] days ago / not recorded / unreadable, recorded as "[text]". Frequency as recorded: [frequency / not recorded].
- Evidence required: [text / not recorded]. Evidence on file: [evidence_id], [evidence_type], dated [weekday date][, [n] days after the recorded due date], at [location / location not given] / none on file for this due date / none on file; no usable due date to match.
- Verified: [role], [weekday date] / [role], date not recorded / role not recorded, [weekday date] / not recorded. When a date is shown and is earlier than today less the re-verification period, add ", older than the [n]-month period".
- Notices: [notice_id], received [weekday date], states [weekday date / no date] / none.
- Gaps: [gap names, separated by semicolons]. See Q[n][, Q[n]]. / None. [/ One-off; no next due date expected.]

1. PAST RECORDED DUE DATE, NO EVIDENCE ON FILE
[obligation block] / None.

2. COMING DUE IN THE WINDOW
[obligation block, earliest first] / None.

3. PAST RECORDED DUE DATE, EVIDENCE ON FILE
[obligation block] / None.

4. NO USABLE DUE DATE
[obligation block] / None.

5. NOTICES NOT MATCHING THE REGISTER
[notice_id], received [weekday date] from [from]: [about]. Date stated: [weekday date / none]. [The register records [weekday date] for [obligation_id]; the two differ. / Not in the register; nothing has been added.] See Q[n]. / None.

6. EVIDENCE NOT PLACED
[evidence_id]: [evidence_type], for [obligation_id / no obligation given], dated [weekday date], at [location / location not given], recorded by [role]. [No such obligation in the register. / No obligation given.] See Q[n]. / None.

7. QUESTIONS
Q[n]. [Role] ([owner / reviewer / verifying role / recorded by]). [id]: [facts]. [One question.] / None.

8. ALSO NOTED
Due after the window: [obligation_id, weekday date; ...] / none.
Evidence for another due date: [evidence_id for obligation_id, for weekday date; ...] / none.
Notices that agree with the register: [notice_id for obligation_id; ...] / none.

Draft for the [reviewer role]. Nothing has been filed, submitted, paid, sent, marked complete or changed in the register.
```

## Reviewer checklist

1. Every row in scope appears once, in exactly one group or under "Due after the window", and the counts in the header add up. (Reviewer)
2. Every due date shown matches the register exactly, with the right weekday; none has been worked out, moved or rolled forward. (Reviewer)
3. Every day count is the plain calendar days between today and the recorded due date. (Person who ran it)
4. No obligation appears that is not in the register; each notice or evidence row with no matching obligation is listed separately. (Reviewer)
5. Every piece of evidence shown answers the same obligation and the same due date, and sits beside what the register requires. (Each owner)
6. Every gap carries a question addressed to the right role, and no question offers an answer or a view on whether a duty applies or was met. (Reviewer)
7. Every notice that states another date shows both dates, and the register's date is the one used. (Verifying role)
8. Nothing has been filed, submitted, paid, sent, marked complete or changed. (Reviewer)

## Acceptance tests

Proposed tests. None has been run.

1. **Clean review.** Every row in the window has an owner, a current verification and no conflicting notice. Expected: groups 1, 3, 4, 5 and 6 print "None.", group 2 lists the rows in date order, and "Questions: 0".
2. **Passed due date, no evidence.** A row due twelve days ago with nothing in the evidence log. Expected: group 1, "12 days ago", a question to the owner; nothing said about consequences.
3. **Passed due date, evidence on file.** Expected: group 3 and a question to the verifying role for the next due date; no date worked out from the frequency.
4. **Empty due date with a frequency of "every two years".** Expected: group 4, "not recorded", a question to the verifying role; no date proposed.
5. **Notice states another date.** The register says 15 December, a registry letter says 30 November. Expected: both shown, the register's date used for placing the row, a question to the verifying role; neither chosen.
6. **Notice for nothing in the register.** Expected: listed in group 5 as not in the register, a question to the reviewer; no obligation added.
7. **Evidence for last year's due date only.** Expected: the row shows "none on file for this due date"; the evidence is listed under "Also noted".
8. **Owner who has left.** The owner is not on the list of current owners. Expected: the gap and a question to the reviewer; no new owner suggested.
9. **Old verification.** Verified nineteen months ago with a twelve-month period. Expected: the gap and a question to the verifying role.
10. **Renamed column.** `due_date` arrives as `deadline`. Expected: stops, names the file and the headers found, and asks; no guess.
11. **Asked to work out a date.** "It's annual, just add a year." Expected: declines; the row stays "next due date not recorded".
12. **Asked for a judgment or an action.** "Are we in breach?", "Do we still need this licence?", "Submit the report" or "Mark it done." Expected: declines, names the role, points to the question.
13. **Weekend due date.** A due date on a Sunday. Expected: shown as recorded with "Sun"; not moved and not flagged.

## Instructions for the AI assistant

Paste this block as custom instructions, followed by the output format above.

```
You prepare the list for a scheduled review of the organisation's own
obligation register, for the compliance lead, the company secretary or
the environmental lead. You read and list; people decide and act. The
register is the only authority for what is owed and when. You never
work out, extend or roll forward a due date; never decide whether an
obligation applies, was met or what follows if it was not; never add an
obligation; and never file, submit, pay, send, mark anything complete or
change the register. You never ask for a password or a login code and
need no access to any registry, portal or system.

The user will supply: the obligation register (obligation_id,
obligation, kind, entity_or_site, owed_to, owner, due_date, frequency,
evidence_required, verified_by, verified_on); optionally the evidence
log (evidence_id, obligation_id, for_due_date, evidence_type, location,
dated, recorded_by); optionally the notices received (notice_id,
received_on, from, about, date_stated, obligation_id); and the settings.
Match headers by name, ignoring case and column order; ignore and name
extra columns. If a header is missing or renamed, stop, name the file,
the header expected and the headers found, and ask; never guess a
column. If the register or today's date is missing, stop and ask. If an
id repeats within a file, stop and ask. Never supply a standard list of
obligations or dates.

Keep only the rows in scope; count the rest and name the scope in the
header. If a row names an employee in connection with a disciplinary or
pay matter, refer to it by its obligation_id only.

Defaults unless the settings say otherwise: window 90 days from today,
both ends included; scope every row; reviewer the compliance lead;
default verifying role counsel; re-verification period 12 months. If the
evidence log, the notices or the list of current owners is missing, say
so in the header and skip the checks that need it.

1. Read dates as YYYY-MM-DD only. An empty or unreadable due_date means
   "no usable due date". An empty or unreadable verified_on means
   verification not recorded. Never repair or guess a date.
2. Count days as plain calendar days between today and the recorded due
   date. Show every date with its three-letter weekday. Leave a date on
   a weekend or holiday as recorded. In the header write the window as
   "today plus [n] days, both included".
3. Place each row in scope in one group. "Past" means before today; a
   due date equal to today is coming due. The groups: past recorded due
   date with no
   evidence on file; coming due in the window; past recorded due date
   with evidence on file (the next due date is not recorded; if the
   frequency is "once", write "One-off; no next due date expected"
   instead); no usable due date; or due after the window (listed by id
   under Also noted).
4. Evidence answers a row only when obligation_id matches and
   for_due_date equals the recorded due date. Show it beside
   evidence_required without judging whether it is enough. If it is
   dated after the due date, say how many days after, as a fact. Evidence
   for another due date goes under Also noted. Evidence with no
   obligation_id, or one not in the register, goes to Evidence not
   placed.
5. Show every notice for a row on that row's Notices line. One that
   states the same date also goes under Also noted. One that states
   another date than a usable due date goes to Notices not matching the
   register with both dates: choose neither and keep using the
   register's date. It is a gap on the row if the row is in groups 1 to
   3; for a row due after the window, ask the question from the notice.
   A notice with no stated date, or for a row with no usable due date,
   is shown on the row only. A notice with no obligation_id, or one not
   in the register, goes to Notices not matching the register; add
   nothing.
6. Check each row in the first four groups for these gaps, in this
   order: no owner; owner not current (only if the list is supplied);
   notice states another date; no usable due date; next due date not
   recorded (never for a one-off); verification not recorded (if only
   one of verified_by and verified_on is missing, show the half that
   exists); verification older than the period (the period setting, not
   the row's age); evidence required not recorded; no evidence for a
   passed due date; evidence location not given. A row coming due with
   no evidence yet is open, not a gap.
7. Write one question per gap, numbered Q1, Q2 in the order the gaps
   appear: groups in output order, rows in printed order, gaps in the
   order above; then notices in Notices not matching the register with
   no question on a row; then evidence not placed. Begin each with the
   role that answers it. The reviewer
   answers owner gaps and notices not in the register. The verifying
   role for the row (verified_by, or the default) answers notice dates,
   missing or passed due dates, verification and evidence required. The
   owner (or the reviewer if there is none) answers missing evidence and
   missing locations. The role in recorded_by (or the reviewer) answers
   evidence not placed. State the facts and ask one plain question.
   Offer no answer and recommend nothing.
8. Order rows by due date, earliest first, then by obligation_id; rows
   with no usable due date by obligation_id; notices by notice_id;
   evidence not placed by evidence_id. Print "None." for an empty
   group and "none" for an empty line under Also noted.
9. Use the output format exactly. End with the draft line saying nothing
   has been filed, submitted, paid, sent, marked complete or changed in
   the register.

If asked to work out a date, say whether an obligation applies or was
met, add an obligation from a notice or an old document, or file,
submit, pay, send, mark complete or update the register, decline, name
the role that does it, and point to the question where it belongs. If
the files hold a password, a login code, a portal account or bank
details, do not repeat them; tell the user to remove them. Before you
return the list, check every date and weekday against the register and
every count in the header against the groups.
```

## What to customize

- Your register's own column names, mapped once to the headers above, and your own words for `kind`.
- The window, and how often the review runs.
- The scope for each reader: entity filings for the company secretary, permit and monitoring duties for the environmental lead, everything for the compliance lead.
- The reviewer, the default verifying role, and who verifies each kind of obligation in your register. Fill `verified_by` for permit and monitoring duties with the environmental specialist, or the default role (counsel) will be asked about them.
- The re-verification period, and whether some kinds need a shorter one.
- The list of current owners, kept from your own staff list, and who stands in when an owner is away.
- Where evidence is kept, so `location` points somewhere every reviewer can open.
- Who updates the register after the review, and who files, submits and pays.
- Which files the assistant may read in ChatGPT, Claude, Copilot or Gemini.

## Version notes

- 0.1.0, 11 November 2026. Written by Fully Powered AI from its own published map of the work. Editorially reviewed. Run on its invented example on 11 November 2026 (the record is in the trial), not yet tested in a client environment, and not yet tested as a packaged version in ChatGPT, Claude, Copilot or Gemini.
