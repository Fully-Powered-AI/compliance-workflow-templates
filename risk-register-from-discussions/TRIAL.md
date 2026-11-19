# Trial: Risk register from risk discussions, run once on its example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-11

The inputs are the example in `public/example.md` (sections 1 to 6 under "The inputs": the review settings, the rating scale, the current register, the incident log and records R1 and R2). No client data was used. The model that ran the template did not write it.

One thing weakens this trial, and it is stated first. The run was meant to be done before the example's published output was read. In practice the example file was opened whole, so the published output was on screen before the draft below was written. The draft was still built step by step from the template's rules and the inputs, and the comparison below is made line by line, but the two outputs are not independent. Read the closeness of the match with that in mind. A run by a reader who has not seen the example would be a stronger test.

## What came out

The full draft, as produced.

**RISK REGISTER DRAFT: Q4 2026 business risk review**

- For: Ruth (Finance director), risk lead. Prepared Friday 20 November 2026 for the leadership meeting, Wednesday 2 December 2026.
- Records: R1, workshop notes, 12 November 2026; attendees Ruth (Finance director), Dana (Operations director), Marek (Head of sales), Wen (IT manager), Tobi (Quality manager); notes by Ilse (Office manager). R2, meeting minutes, 17 November 2026; attendees Sam (Managing director), Ruth (Finance director), Dana (Operations director), Marek (Head of sales); notes by Ruth (Finance director). Lines were numbered in the records as supplied.
- Also supplied: current register (5 risks, last reviewed 20 May 2026); incident log (4 incidents); rating scale with an escalation rule.
- Counts: 5 entries (2 matching the current register, 3 new). 2 raised but not entered. 3 register risks not discussed. 4 incidents: 1 attached, 3 not linked. 10 questions.

**DRAFT ENTRIES**

**D01.** Supplier A, which makes all the company's cast pump housings, has a fire or goes under, and the company stops building pumps.
- Raised by: Dana (Operations director), R1 line 2. Also discussed by: Tobi (Quality manager), R1 line 4; Ruth (Finance director), R1 line 6 and R2 line 2.
- Cause: Supplier A is the only maker of the company's cast pump housings (Dana, R1 line 2).
- Current register: R-02, Sole supplier of cast housings fails. Owner: Operations director. Rating 2 × 5 = 10, last reviewed 2026-05-20.
- Existing controls:
  - About three weeks of safety stock of housings. Said by Dana, R1 lines 2 and 3. In current register R-02; evidence named there: weekly stock report (not examined).
  - Quarterly review of Supplier A. Said by Dana, R1 line 3. In current register R-02; evidence named there: supplier review minutes (not examined). Contested: Tobi, R1 line 4: "We haven't actually held the Supplier A review since June." See Q2.
  - Controls in the current register not mentioned: none.
- Proposed mitigations:
  - Qualify Supplier C as a second foundry. Proposed by Dana, R1 line 5 ("I can own qualifying Supplier C"). Owner: Dana (Operations director), as offered. Date: starting in January. Proposed, not approved.
  - Raise housing safety stock to six weeks. Proposed by Ruth, R2 line 2. Owner: not named. Date: not stated. Cost: about £90,000 of working capital. Proposed, not approved.
- Owner of the risk: Operations director, from current register R-02; ownership not discussed.
- Rating: Stated: Ruth, R1 line 6: 3 × 5 = 15; Dana, R1 line 7: 2 × 5 = 10. Suggested: likelihood not matched: no frequency was stated, and "solid for twelve years" (Dana, R1 line 7) describes a record, not a frequency; impact 5, from "about three weeks of housings" and "four to six months" to qualify a new foundry (Dana, R1 line 2): four months less three weeks of stock is well over two weeks of stopped production, which is inside level 5; no suggested rating.
- Incidents: INC-046, 2026-10-14: Supplier A delivery of housings arrived four days late. Linked to R-02 in the log.
- Open questions: Q1, Q2.

**D02.** Customer B, 38% of revenue, has a contract that renews on 31 March and a new buyer who has opened a tender; losing half of Customer B's volume would lose around £400,000 of gross margin a year.
- Raised by: Marek (Head of sales), R1 line 8. Also discussed by: Sam (Managing director), R2 line 1.
- Cause: Customer B's new buyer has opened a tender (Marek, R1 line 8).
- Current register: R-01, Loss of a major customer. Owner: Head of sales. Rating 3 × 4 = 12, last reviewed 2026-05-20.
- Existing controls:
  - Account plan for Customer B. Said by Marek, R1 line 9. In current register R-01; evidence named there: CRM account plans (not examined).
  - Quarterly reviews with Customer B. Said by Marek, R1 line 9. Stated only; no evidence supplied.
  - Controls in the current register not mentioned: none.
- Proposed mitigations:
  - Get the tender response and a cost-down offer ready. Proposed by Marek, R1 line 9. Owner: Marek (Head of sales). Date: by 15 December. Proposed, not approved.
- Owner of the risk: Head of sales, from current register R-01; ownership not discussed.
- Rating: Stated: none stated. Suggested: likelihood not matched: no frequency was stated; impact 4, from "around £400,000 of gross margin a year" (Sam, R2 line 1), which falls inside £250,000 to £1,000,000 (the figure is for losing half of the volume, not the whole customer); no suggested rating.
- Incidents: none.
- Open questions: Q3.

**D03.** The ERP server stops, and dispatch stops for most of a shift.
- Raised by: Wen (IT manager), R1 line 10. Also discussed by: Ruth (Finance director), R1 line 11.
- Cause: the server is nine years old and out of warranty (Wen, R1 line 10).
- Current register: new: not in the current register.
- Existing controls:
  - Nightly backup of the ERP to the cloud. Said by Wen, R1 line 12. Stated only; no evidence supplied.
- Proposed mitigations:
  - Replace the server or move to a hosted ERP. Proposed by Wen, R1 line 12 (quotes due in December). Owner: not named (Wen said he is getting the quotes, which is not the same as owning the replacement). Date: not stated. Proposed, not approved.
- Owner of the risk: not named.
- Rating: Stated: none stated. Suggested: likelihood 5, from "stopped three times this year" (Wen, R1 line 10), which is more than once a year; impact 1, from "about £6,000" for each stoppage (Ruth, R1 line 11), which is under £10,000; rating 5 × 1 = 5, suggested, for the owner of the risk to confirm.
- Incidents: none attached (see the incidents section below).
- Open questions: Q4, Q10.

**D04.** A sales laptop holding a customer contact spreadsheet is lost, customer data leaks, and the company faces a complaint.
- Raised by: Marek (Head of sales), R1 line 13. Also discussed by: Wen (IT manager), R1 lines 14 and 17; Ruth (Finance director), R1 line 16.
- Cause: sales keep customer contact lists in their own spreadsheets on their laptops (Marek, R1 line 13).
- Current register: new: not in the current register.
- Existing controls:
  - All laptops are encrypted. Said by Wen, R1 line 14. Stated only; no evidence supplied. Contested: Marek, R1 line 15: "Not the two older sales laptops. They were never reissued." See Q5.
- Proposed mitigations: none proposed.
- Owner of the risk: proposed by Ruth at R1 line 16; not confirmed by Wen, who said at R1 line 17 that he would need sales to own the spreadsheets.
- Rating: Stated: none stated. Suggested: likelihood not matched: no frequency was stated; impact not matched: no cost or duration was stated; no suggested rating.
- Incidents: none.
- Open questions: Q5, Q6.

**D05.** The senior estimator leaves, nobody else can price the large pumps, and large pumps are about a quarter of new orders. The record names the senior estimator; this entry refers to the role.
- Raised by: Marek (Head of sales), R1 line 18. Also discussed by: no one else.
- Cause: only the senior estimator can price the large pumps (Marek, R1 line 18).
- Current register: new: not in the current register.
- Existing controls: none stated.
- Proposed mitigations: none proposed.
- Owner of the risk: not named.
- Rating: Stated: none stated. Suggested: likelihood not matched: no frequency was stated; impact not matched: "about a quarter of our new orders" is a share of orders, not a cost or a duration; no suggested rating.
- Incidents: none.
- Open questions: Q7.

**RAISED BUT NOT ENTERED**

- Tobi (Quality manager), R1 line 19: "Quality is a worry generally." Reason: no event or effect stated. See Q8.
- Sam (Managing director), R2 line 3: "We already lost the Customer D order last month because of late deliveries." Reason: already happened. See Q9.

**IN THE CURRENT REGISTER, NOT DISCUSSED**

- R-03, Fire at the main site. Owner: Operations director. Rating 1 × 5 = 5. Unchanged.
- R-04, Product recall from a field failure. Owner: Quality manager. Rating 2 × 4 = 8. Unchanged.
- R-05, Exchange-rate movement on euro purchases. Owner: Finance director. Rating 3 × 2 = 6. Unchanged.

**INCIDENTS NOT LINKED TO AN ENTRY**

- INC-031, 2026-02-11: ERP server stopped; dispatch halted for most of the late shift. See Q10.
- INC-038, 2026-06-23: ERP server stopped; dispatch halted for five hours. See Q10.
- INC-044, 2026-09-30: ERP server stopped after a power dip; dispatch halted for most of the day shift. See Q10.

**QUESTIONS**

Q1. To Ruth (Finance director), risk lead, who gave a stated rating on D01. You stated likelihood 3, impact 5, rating 15 (R1 line 6); Dana stated likelihood 2, impact 5, rating 10 (R1 line 7); the current register carries 10. No stated frequency matches a likelihood level. Which likelihood does the register carry? Your proposal to raise housing safety stock to six weeks, about £90,000 of working capital (R2 line 2), has no owner. Who would own it if it is approved?

Q2. To Dana (Operations director), who gave a stated rating on D01 and is owner of R-02. You stated likelihood 2 where Ruth stated 3 (R1 lines 6 and 7). Which likelihood do you stand by? The register lists a quarterly review of Supplier A as a control, with supplier review minutes as its evidence; Tobi said it has not been held since June (R1 line 4). Is the review in operation, and when was it last held?

Q3. To Ruth (Finance director), risk lead. D02: impact matches level 4 from Sam's figure of around £400,000 a year, which is for half of Customer B's volume (R2 line 1); no stated frequency matches a likelihood level and no rating was stated. What likelihood does the register carry?

Q4. To Ruth (Finance director), risk lead. D03: no owner of the risk was named, and no owner was named for replacing the server or moving to a hosted ERP (R1 line 12). Who owns the risk, and who owns that proposal?

Q5. To Ruth (Finance director), risk lead. D04: Wen said all laptops are encrypted (R1 line 14); Marek said the two older sales laptops are not (R1 line 15). You proposed Wen as owner (R1 line 16); Wen said sales would need to own the spreadsheets (R1 line 17). No frequency, cost or duration was stated. Which laptops are encrypted, who owns the risk, and what likelihood and impact does the register carry?

Q6. To counsel, through Ruth (Finance director). D04 concerns customer data on lost laptops. Would a loss of that data create a legal duty for the company? This draft does not say.

Q7. To Ruth (Finance director), risk lead. D05: no owner was named, and no frequency, cost or duration was stated. Who owns the risk, and what likelihood and impact does the register carry?

Q8. To Tobi (Quality manager). R1 line 19: "Quality is a worry generally." What could go wrong, and what would it do to the business?

Q9. To Sam (Managing director). R2 line 3: the Customer D order lost last month because of late deliveries. Is there something that could happen next that you want on the register? If so, what is it and what would it do to the business?

Q10. To Wen (IT manager), who raised D03. INC-031 (2026-02-11), INC-038 (2026-06-23) and INC-044 (2026-09-30) record the ERP server stopping and are linked to no risk in the log. Do they belong to D03, and are they the three stoppages you described at R1 line 10?

**FOR AUTHORISED LEADERS**

Escalation rule: a rating of 15 or more goes to the board's risk committee, which decides whether the risk is treated, funded or accepted.

- D01, Supplier A fails: Ruth's stated rating of 15 (R1 line 6) meets the rule; Dana stated 10 (R1 line 7), and the current register carries 10. Proposed mitigation with a stated cost: raising housing safety stock to six weeks, about £90,000 of working capital (R2 line 2). Decided by: the board's risk committee.

Rated and below the rule: D03, suggested 5.

Not rated, so not checked against the rule: D02, D04, D05.

Draft for Ruth, risk lead. Every entry traces to the records named above. Nothing has been added to the register, assigned, accepted or sent.

## What was observed

What worked.

- Every part of the output format was produced, in the order given, with "none" where a section was empty. The counts in the header (5 entries, 2 raised but not entered, 3 register risks not discussed, 4 incidents, 10 questions) match the sections below them.
- Nothing the template says to stop for came up. The record had a risk lead and a number on every line, and both exports had the expected headers. No statement was unattributed, no record held a password, and nothing asked the assistant to add a risk, rate without the scale, assign an owner or say whether the company complies with a law.
- The company's scale was applied only where a stated figure fell inside one level. Two entries (D03, and D01's impact) were matched with the working shown; the rest were marked "not matched" with the reason, and no word such as high, medium or low was used.
- The differing ratings on Supplier A and the contested review and encryption claims were shown on both sides, and no choice was made between them.
- The counsel question was asked and not answered. The senior estimator was referred to by role only.
- The three unlinked ERP incidents were not attached to the ERP entry. No speaker cited them by number or date, and the entry matches no register row, so the template's tests for attaching were not met; they were listed and put to the person who raised the entry.

Where the instructions needed a judgement, or were silent.

1. **Merging on one effect.** Marek's line about Customer B states an event (a tender before renewal) but no effect; Sam's later line states an effect for a different event (losing half the volume). The template lets an effect come from several speakers on the same event, but does not say whether "a tender" and "losing half the volume" are the same event. They were merged, and the sentence for D02 keeps both.
2. **What "cause" means.** The template asks for the cause where one was stated, but does not separate a cause from a condition. "Supplier A is the only maker" was entered as the cause of D01; the four to six months to qualify a new foundry was kept for the impact working instead.
3. **Owning a mitigation.** "I can own qualifying Supplier C" is an offer, and "I'm getting quotes" is part of a task, not ownership of the replacement. The template says to use the owner as stated, and does not say how to treat an offer or a part. The first was entered as "as offered", the second as "not named" with the quote remark.
4. **Rating a frequency from a record.** "Solid for twelve years" and "stopped three times this year" are both about the past. The template allows a likelihood level only from a stated frequency. The second was accepted as more than once a year; the first was not treated as a frequency. A reader could decide either differently, and nothing in the template says how to treat a count over part of a year or a run with no event.
5. **Gross margin and dispatch against the scale's wording.** The scale defines impact as the cost of one occurrence over twelve months, or how long production stops. Sam's figure is gross margin lost on half a customer's volume. The ERP figure is overtime and late-delivery charges while dispatch (not production) stops. The template does not say whether these count as costs or durations in the scale's sense. Both were accepted as costs, and the half-volume point was written into the entry and its question.
6. **One question or two for the risk lead.** Ruth is the risk lead and also gave a stated rating. The template sends differing ratings to the people who gave them and other gaps to the risk lead. Her gaps for D01 were put in one question, and Dana's in another. The template does not say what to do when the two roles are one person, and it does not say how to treat the owner of a register row that is given only as a role (Operations director). Here the attendee list made that Dana.
7. **Question order.** Questions run in entry order, then items not entered, then incidents, so the question about the ERP incidents (Q10) is last although it concerns D03.
8. **"Also discussed by".** It is not stated whether a later line by the first speaker (Dana on D01, R1 line 3) belongs in this list. The first speaker's further lines were cited under the controls instead.
9. **Roles in the instruction block.** The fenced block is shorter than the procedure and numbered differently from it (twelve steps against fourteen). Nothing in the block contradicted the procedure in this run, but a reader following the block alone has less to go on for items such as how to word an owner of a risk and when an incident counts as cited.

Differences from the published example's output.

- The two are very close. Entry numbering, matches, ratings, escalation list, section contents and counts agree, and both reach 10 questions. Given the lapse at the top, this is not strong evidence that two independent runs would agree.
- Small differences in wording. The D02 sentence opens with the contract renewal and the tender where the example opens with the share of revenue. The D01 cause here is the sole source alone, where the example also gave the qualifying time. D01's impact working is worded differently but reaches level 5 on the same figures. D03's mitigation owner carries a remark about the quotes. The Supplier C owner is marked "as offered". The impact note on D02 says the figure is for half the volume. Q2 asks which likelihood Dana stands by, where the example asked which the register carries. Q10 asks first whether the incidents belong to D03. Dates in the register and incident lines are written as in the exports (2026-05-20), where the example spells them out.
- Differences in structure. The example's counts line and sections are the same as here; this draft adds the sentence "Lines were numbered in the records as supplied" to the records line, which the template only asks for when the assistant did the numbering.

Facts not in the inputs. None was found in either output. Every name, figure, date and quotation in both can be found in the inputs. Two inferences are made in both and are not stated by a speaker: that the Operations director on the register is Dana (from the attendee list), and that "most of a shift" is the effect to enter for the ERP server.

Shortcomings. This was one run, by one model, on an example written by the same company, and the run was not blind to the example's output. It tests that the template can be followed to a complete and consistent draft on a case built to exercise it. It does not show that the draft would suit a real register, a real scale, a long transcript, or a model other than the one used.

## After the run

After this run the template was revised without being run again. It now settles, in one sentence each, how to tell a recurring condition from a past event, whether a trigger and the loss it leads to are one event, how to treat an offered or partial owner of a mitigation, the risk lead who is also a rating giver, a register owner given only as a role, and the first speaker's later lines. It also states the "pairing unclear", question-order, unattributed-line and disagreeing-records rules in the instruction block, and says to write "if ..." when a figure assumes the event lasts a stated time. The example's D01 impact wording was changed to match. The record above is of the earlier wording and has not been altered; the revised template has not been run. A later review round added further sentences to the template and corrected three small points in the example; those changes have not been run either.
