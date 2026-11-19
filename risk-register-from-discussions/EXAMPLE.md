# Risk register from risk discussions: an example

*Illustrative example with sample data.* The company, the people, the suppliers, the customers, the incidents and every figure below are illustrative. The company is an illustrative 140-person maker of industrial pumps, called "the company" here. Its finance director, Ruth, is the risk lead and keeps the risk register. First come the inputs Ruth supplied, in full, then the draft the workflow template returned.

## The inputs

### 1. Review settings

```
Review: Q4 2026 business risk review
Risk lead: Ruth (Finance director)
Draft is for: leadership meeting, Wednesday 2 December 2026
Today: Friday 20 November 2026
```

### 2. Rating scale (the company's own)

```
Likelihood: how often we would expect it
  1  Less than once in 10 years
  2  Once in 5 to 10 years
  3  Once in 1 to 5 years
  4  About once a year
  5  More than once a year

Impact: the cost of one occurrence over the following twelve months,
or how long production stops
  1  Under £10,000
  2  £10,000 to £50,000
  3  £50,000 to £250,000
  4  £250,000 to £1,000,000
  5  Over £1,000,000, or production stopped for more than two weeks

Rating: likelihood x impact.
Escalation: a rating of 15 or more goes to the board's risk committee,
which decides whether the risk is treated, funded or accepted.
```

### 3. Current risk register (export)

```
risk_id,risk,owner,controls,control_evidence,likelihood,impact,rating,last_reviewed
R-01,Loss of a major customer,Head of sales,Account plans for top five customers,CRM account plans,3,4,12,2026-05-20
R-02,Sole supplier of cast housings fails,Operations director,Safety stock of housings; quarterly supplier review,Weekly stock report; supplier review minutes,2,5,10,2026-05-20
R-03,Fire at the main site,Operations director,Sprinklers; annual fire inspection,Inspection certificate,1,5,5,2026-05-20
R-04,Product recall from a field failure,Quality manager,Final test of every pump; batch traceability,Test records; traceability log,2,4,8,2026-05-20
R-05,Exchange-rate movement on euro purchases,Finance director,Forward contracts for six months of purchases,Treasury file,3,2,6,2026-05-20
```

### 4. Incident log (export)

```
incident_id,date,summary,linked_risk_id
INC-031,2026-02-11,ERP server stopped; dispatch halted for most of the late shift,
INC-038,2026-06-23,ERP server stopped; dispatch halted for five hours,
INC-044,2026-09-30,ERP server stopped after a power dip; dispatch halted for most of the day shift,
INC-046,2026-10-14,Supplier A delivery of housings arrived four days late,R-02
```

### 5. Record R1: risk workshop notes

```
Record: R1
Type: workshop notes
Date: 12 November 2026
Attendees: Ruth (Finance director); Dana (Operations director); Marek (Head of sales); Wen (IT manager); Tobi (Quality manager)
Notes by: Ilse (Office manager)

1  Ruth: The purpose is to refresh the register before the 2 December leadership meeting.
2  Dana: Supplier A makes all our cast pump housings. If they had a fire or went under, we would stop building pumps. We hold about three weeks of housings, and qualifying a new foundry takes four to six months.
3  Dana: The three weeks of safety stock is our protection. We also review Supplier A every quarter.
4  Tobi: We haven't actually held the Supplier A review since June.
5  Dana: I can own qualifying Supplier C as a second foundry, starting in January.
6  Ruth: I'd put the Supplier A risk at likelihood 3, impact 5.
7  Dana: Impact 5, yes, but likelihood 2. They've been solid for twelve years.
8  Marek: Customer B is 38% of our revenue. Their contract renews on 31 March and their new buyer has opened a tender.
9  Marek: We have an account plan and quarterly reviews with them. I'll own getting the tender response and a cost-down offer ready by 15 December.
10 Wen: The ERP server is nine years old and out of warranty. It has stopped three times this year, and each time dispatch stopped for most of a shift.
11 Ruth: Each of those stoppages cost us about £6,000 in overtime and late-delivery charges.
12 Wen: We back the ERP up to the cloud every night. I'm getting quotes to replace the server or move to a hosted ERP; they're due in December.
13 Marek: Sales keep customer contact lists in their own spreadsheets on their laptops. If one of those laptops is lost, customer data could leak and we could face a complaint.
14 Wen: All laptops are encrypted.
15 Marek: Not the two older sales laptops. They were never reissued.
16 Ruth: Wen, can you own the laptop risk?
17 Wen: I'd need sales to own the spreadsheets.
18 Marek: If Jo, our senior estimator, left, nobody else could price the large pumps, and large pumps are about a quarter of our new orders.
19 Tobi: Quality is a worry generally.
20 Ruth: Owners to be confirmed at the leadership meeting.
```

### 6. Record R2: leadership meeting minutes (extract)

```
Record: R2
Type: meeting minutes
Date: 17 November 2026
Attendees: Sam (Managing director); Ruth (Finance director); Dana (Operations director); Marek (Head of sales)
Notes by: Ruth (Finance director)

1  Sam: If we lost half of Customer B's volume, we would lose around £400,000 of gross margin a year.
2  Ruth: For Supplier A, we could raise housing safety stock to six weeks. That would tie up about £90,000 of working capital.
3  Sam: We already lost the Customer D order last month because of late deliveries.
```

## The output

**RISK REGISTER DRAFT: Q4 2026 business risk review**

- For: Ruth (Finance director), risk lead. Prepared Friday 20 November 2026 for the leadership meeting, Wednesday 2 December 2026.
- Records: R1, workshop notes, 12 November 2026; attendees Ruth (Finance director), Dana (Operations director), Marek (Head of sales), Wen (IT manager), Tobi (Quality manager); notes by Ilse (Office manager). R2, meeting minutes, 17 November 2026; attendees Sam (Managing director), Ruth (Finance director), Dana (Operations director), Marek (Head of sales); notes by Ruth (Finance director).
- Also supplied: current register (5 risks, last reviewed 20 May 2026); incident log (4 incidents); rating scale with an escalation rule.
- Counts: 5 entries (2 matching the current register, 3 new). 2 raised but not entered. 3 register risks not discussed. 4 incidents: 1 attached, 3 not linked. 10 questions.

**DRAFT ENTRIES**

**D01.** Supplier A, which makes all the company's cast pump housings, has a fire or goes under, and the company stops building pumps.
- Raised by: Dana (Operations director), R1 line 2. Also discussed by: Tobi (Quality manager), R1 line 4; Ruth (Finance director), R1 line 6 and R2 line 2.
- Cause: Supplier A makes all the company's cast pump housings, and qualifying a new foundry takes four to six months (Dana, R1 line 2).
- Current register: R-02, Sole supplier of cast housings fails. Owner: Operations director. Rating 2 × 5 = 10, last reviewed 20 May 2026.
- Existing controls:
  - About three weeks of safety stock of housings. Said by Dana, R1 lines 2 and 3. In current register R-02; evidence named there: weekly stock report (not examined).
  - Quarterly review of Supplier A. Said by Dana, R1 line 3. In current register R-02; evidence named there: supplier review minutes (not examined). Contested: Tobi, R1 line 4: "We haven't actually held the Supplier A review since June." See Q2.
  - Controls in the current register not mentioned: none.
- Proposed mitigations:
  - Qualify Supplier C as a second foundry. Proposed by Dana, R1 line 5. Owner: Dana (Operations director), as offered. Date: starting in January. Proposed, not approved.
  - Raise housing safety stock to six weeks. Proposed by Ruth, R2 line 2. Owner: not named. Date: not stated. Cost: about £90,000 of working capital. Proposed, not approved.
- Owner of the risk: Operations director, from current register R-02; ownership not discussed.
- Rating: Stated: Ruth, R1 line 6: 3 × 5 = 15; Dana, R1 line 7: 2 × 5 = 10. Suggested: likelihood not matched: no frequency was stated, and "solid for twelve years" (Dana, R1 line 7) is not a frequency; impact 5, if Supplier A does not resume within that time, from "we would stop building pumps", "about three weeks of housings" and "four to six months" (Dana, R1 line 2): even the shortest stated time, four months, less three weeks of stock leaves production stopped for more than two weeks; no suggested rating.
- Incidents: INC-046, 14 October 2026: Supplier A delivery of housings arrived four days late. Linked to R-02 in the log.
- Open questions: Q1, Q2.

**D02.** Customer B, 38% of revenue, has a contract that renews on 31 March and a new buyer who has opened a tender; losing half of Customer B's volume would lose around £400,000 of gross margin a year.
- Raised by: Marek (Head of sales), R1 line 8. Also discussed by: Sam (Managing director), R2 line 1.
- Cause: Customer B's new buyer has opened a tender (Marek, R1 line 8).
- Current register: R-01, Loss of a major customer. Owner: Head of sales. Rating 3 × 4 = 12, last reviewed 20 May 2026.
- Existing controls:
  - Account plan for Customer B. Said by Marek, R1 line 9. In current register R-01; evidence named there: CRM account plans (not examined).
  - Quarterly reviews with Customer B. Said by Marek, R1 line 9. Stated only; no evidence supplied.
  - Controls in the current register not mentioned: none.
- Proposed mitigations:
  - Get the tender response and a cost-down offer ready. Proposed by Marek, R1 line 9. Owner: Marek (Head of sales). Date: by 15 December. Proposed, not approved.
- Owner of the risk: Head of sales, from current register R-01; ownership not discussed.
- Rating: Stated: none stated. Suggested: likelihood not matched: no frequency was stated; impact 4, from "around £400,000 of gross margin a year" (Sam, R2 line 1), which falls inside £250,000 to £1,000,000, reading gross margin lost as a cost; no suggested rating.
- Incidents: none.
- Open questions: Q3.

**D03.** The ERP server stops, and dispatch stops for most of a shift.
- Raised by: Wen (IT manager), R1 line 10. Also discussed by: Ruth (Finance director), R1 line 11.
- Cause: the server is nine years old and out of warranty (Wen, R1 line 10).
- Current register: new: not in the current register.
- Existing controls:
  - Nightly backup of the ERP to the cloud. Said by Wen, R1 line 12. Stated only; no evidence supplied.
- Proposed mitigations:
  - Replace the server or move to a hosted ERP; quotes due in December. Proposed by Wen, R1 line 12. Owner: not named; Wen is getting the quotes (R1 line 12), which is only a part of the work. Date: not stated. Proposed, not approved.
- Owner of the risk: not named.
- Rating: Stated: none stated. Suggested: likelihood 5, from "stopped three times this year" (Wen, R1 line 10), which is more than once a year; impact 1, from "about £6,000" for each stoppage (Ruth, R1 line 11), which is under £10,000, reading charges while dispatch stops as a cost; rating 5 × 1 = 5, suggested, for the owner of the risk to confirm.
- Incidents: none.
- Open questions: Q4, Q10.

**D04.** A sales laptop holding a customer contact spreadsheet is lost, customer data leaks, and the company faces a complaint.
- Raised by: Marek (Head of sales), R1 line 13. Also discussed by: Wen (IT manager), R1 lines 14 and 17; Ruth (Finance director), R1 line 16.
- Cause: sales keep customer contact lists in their own spreadsheets on their laptops (Marek, R1 line 13).
- Current register: new: not in the current register.
- Existing controls:
  - All laptops are encrypted. Said by Wen, R1 line 14. Stated only; no evidence supplied. Contested: Marek, R1 line 15: "Not the two older sales laptops. They were never reissued." See Q5.
- Proposed mitigations: none proposed.
- Owner of the risk: proposed by Ruth at R1 line 16; not confirmed by Wen, who said at R1 line 17 that sales would need to own the spreadsheets.
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

- INC-031, 11 February 2026: ERP server stopped; dispatch halted for most of the late shift. See Q10.
- INC-038, 23 June 2026: ERP server stopped; dispatch halted for five hours. See Q10.
- INC-044, 30 September 2026: ERP server stopped after a power dip; dispatch halted for most of the day shift. See Q10.

**QUESTIONS**

Q1. To Ruth (Finance director), risk lead. D01: you stated likelihood 3, impact 5, rating 15 (R1 line 6); Dana stated likelihood 2, impact 5, rating 10 (R1 line 7); the current register carries 10. No stated frequency matches a likelihood level. Which likelihood does the register carry? Your proposal to raise housing safety stock to six weeks, about £90,000 of working capital (R2 line 2), has no owner. Who would own it if it is approved?

Q2. To Dana (Operations director), owner of R-02. D01: you stated likelihood 2 where Ruth stated 3 (R1 lines 6 and 7). Which likelihood does the register carry? The register lists a quarterly review of Supplier A as a control, with supplier review minutes as its evidence; Tobi said it has not been held since June (R1 line 4). Is the review in operation, and when was it last held?

Q3. To Ruth (Finance director), risk lead. D02: impact matches level 4 from Sam's figure of around £400,000 a year (R2 line 1); no stated frequency matches a likelihood level and no rating was stated. What likelihood does the register carry, and does gross margin lost count as a cost in your impact definition?

Q4. To Ruth (Finance director), risk lead. D03: no owner of the risk was named, and no owner was named for replacing the server or moving to a hosted ERP (R1 line 12). Who owns the risk, and who owns that proposal? Do charges while dispatch stops count as a cost in your impact definition?

Q5. To Ruth (Finance director), risk lead. D04: Wen said all laptops are encrypted (R1 line 14); Marek said the two older sales laptops are not (R1 line 15). You proposed Wen as owner (R1 line 16); Wen said sales would need to own the spreadsheets (R1 line 17). No frequency, cost or duration was stated. Which laptops are encrypted, who owns the risk, and what likelihood and impact does the register carry?

Q6. To counsel, through Ruth (Finance director). D04 concerns customer data on lost laptops. Would a loss of that data create a legal duty for the company? This draft does not say.

Q7. To Ruth (Finance director), risk lead. D05: no owner was named, and no frequency, cost or duration was stated. Who owns the risk, and what likelihood and impact does the register carry?

Q8. To Tobi (Quality manager). R1 line 19: "Quality is a worry generally." What could go wrong, and what would it do to the business?

Q9. To Sam (Managing director). R2 line 3: the Customer D order lost last month because of late deliveries. Is there something that could happen next that you want on the register? If so, what is it and what would it do to the business?

Q10. To Wen (IT manager), who raised D03. INC-031 (11 February 2026), INC-038 (23 June 2026) and INC-044 (30 September 2026) record the ERP server stopping and are linked to no risk in the log. Are they the three stoppages you described at R1 line 10?

**FOR AUTHORISED LEADERS**

Escalation rule: a rating of 15 or more goes to the board's risk committee, which decides whether the risk is treated, funded or accepted.

- D01, Supplier A fails: Ruth's stated rating of 15 (R1 line 6) meets the rule; Dana stated 10 (R1 line 7), and the current register carries 10. Proposed mitigations with a stated cost: raising housing safety stock to six weeks, about £90,000 of working capital (R2 line 2). Decided by: the board's risk committee.

Rated and below the rule: D03, suggested 5.

Not rated, so not checked against the rule: D02, D04, D05.

Draft for Ruth, risk lead. Every entry traces to the records named above. Nothing has been added to the register, assigned, accepted or sent.
