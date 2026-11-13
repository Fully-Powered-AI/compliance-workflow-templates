# Obligation and filing calendar review: one trial on the invented example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-11

The inputs were the invented example's own: its settings, a ten-row obligation register, a five-row evidence log and three notices, all listed in [the example](example.md). No client data was used. This is the second run on those inputs, made after the instruction block and output format were revised on the same day (the window wording, the Verified line, the Evidence line for a row with no usable due date, the group range for the notice gap, bullets for the obligation block, and two rules added to the block). The record of the first run, which found those ambiguities, is replaced by this one. The run followed the revised instruction block and output format with the inputs only; the example's own output was read afterwards, for comparison. One run, by one model, with no second run to see whether it repeats.

## What came out

The list came out in the template's eight sections. Its header read: for the Compliance lead; prepared Wed 2026-11-11; window Wed 2026-11-11 to Tue 2027-02-09 (today plus 90 days, both included); scope every row; ten rows in scope. Counts: past due with no evidence 1, coming due 6, past due with evidence 1, no usable due date 1, due after the window 1, questions 11.

- **Past due, no evidence:** OB-04, due Fri 2026-10-30, 12 days ago. One question, to its owner, asking where the evidence of completion for that due date is.
- **Coming due:** OB-01 (a notice from Registry A states Mon 2026-11-30 against the register's Tue 2026-12-15, so a question to counsel), OB-05 (no owner, a question to the reviewer), OB-03 (no gaps), OB-07 (verification not recorded, and evidence with no location: two questions), OB-02 (last verified Tue 2025-06-10, older than the 12-month period: a question to counsel) and OB-10 (owner not on the current list: a question to the reviewer).
- **Past due, evidence on file:** OB-08, with the next due date not recorded and a question to the Environmental specialist. No date was worked out from "annual".
- **No usable due date:** OB-09, frequency every two years, with the Evidence line reading "none on file; no usable due date to match". A question, no date proposed.
- **Notices not matching:** N-1 with both dates, and N-2, which names no obligation, with nothing added.
- **Evidence not placed:** EV-04, for OB-12, which is not in the register.
- **Also noted:** OB-06 due Mon 2027-03-01; EV-02, which answers a 2025 due date of OB-03; N-3, which agrees with OB-02.

It ended with the line that nothing has been filed, submitted, paid, sent, marked complete or changed in the register. No instruction asked it to stop, and it did not stop: every header matched, no id repeated, and the register, today's date and the settings were all present.

## What was observed

- **Every required part was produced:** the header with its counts, the five groups, notices not matching, evidence not placed, the numbered questions with a named role first, the also-noted lines and the closing line. The counts add up to the ten rows in scope.
- **Weekdays and day counts were checked** with a date calculation and agreed with the register's dates: 34, 39, 50, 65, 81 and 86 days ahead, 12 and 42 days back, and the window end of Tue 2027-02-09.
- **Differences from the published example:** the facts, groups, counts, gap names, question numbers, question roles and ordering were the same, and the obligation block is now printed with bullets as the example does. Only some question wording differed. I found no fact in either output that is not in the inputs.
- **Where the instructions still left a choice:**
  - For OB-07 the verifying role was empty, so the default (counsel) answers, although the template's own roles section says permit and monitoring duties usually go to the environmental specialist. I followed the literal rule.
  - The window wording, the "older than the 12-month period" wording and the Evidence line for a row with no usable due date were all covered by the revised text. The new wording for a row where only one of `verified_by` and `verified_on` is missing was not exercised, because no row in this example needed it.
- **Shortcomings:** the trial covers the happy path only. It did not test a renamed column, a repeated id, a request to work out a date or to file something, or a missing evidence log, and the template's own acceptance tests, which say none has been run, were not run here. The inputs are small (ten rows), so how it behaves on a register of hundreds was not tried. The run was made by the same model that revised the template, with the example's output in the same working session, so it is a weaker check than a run by a fresh reader.
