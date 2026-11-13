---
name: "obligation-and-filing-calendar-review"
description: "Prepare the list for one scheduled review of the organisation's obligation register: every obligation, filing and renewal in scope whose recorded due date falls in the review window or has already passed, each with its owner, its due date exactly as the register records it, the evidence of completion on file, who verified the entry and when, any notice that bears on it, and every gap written as a numbered question for a named role. The register is the only authority for what is owed and when. The assistant reads and lists; it never works out a due date, never decides whether an obligation applies, never adds an obligation, and never files, submits, pays, sends, marks anything complete or changes the register."
license: "MIT"
metadata:
  version: "0.1.0"
  publisher: "Fully Powered AI"
  template: "Obligation and filing calendar review"
---

# Obligation and filing calendar review

This is the technical file for a Fully Powered workflow template. It carries the instructions an AI product follows. The complete template, with roles, inputs, exceptions, the reviewer checklist, acceptance tests and what to customize, is in [TEMPLATE.md](TEMPLATE.md). A worked example with invented data is in [EXAMPLE.md](EXAMPLE.md).

## Instructions

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

## Before relying on it

Decide every item under "What to customize" in TEMPLATE.md and set the limits the instructions in this file leave open, written in square brackets such as [N], to your own. Then run the acceptance tests in TEMPLATE.md on past work. A person starts this work, supplies the inputs and decides what happens with the result.
