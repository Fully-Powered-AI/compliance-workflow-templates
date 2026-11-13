# Audit finding closure evidence: an invented example

*Illustrative example with invented data.* The company, the people, the finding, the systems, the records and the dates below are all invented. The company is an invented 140-person payments software business with a small internal audit team. In the spring, internal audit raised a finding about people who had left keeping access to two internal systems. In November the IT operations manager reports the agreed actions complete and asks for the finding to be closed. The compliance lead runs the workflow template before the head of internal audit decides. First come the inputs the compliance lead supplied, in full, then the comparison the workflow template returned.

## The inputs

### 1. Settings

```
Today: 4 November 2026
Compliance lead: Compliance lead
Closure decided by: Head of internal audit
```

### 2. The finding record (from the findings tracker)

```
finding_id: IA-2026-07
title: Leavers keep access to the payments admin console
condition: In a sample of 25 people who left between 1 January and 31 March 2026, 4 still had active accounts on the payments admin console or the customer support tool between 6 and 19 working days after their last day.
criterion: Access control standard AC-02, revision 3, section 4: access to production systems is removed by the end of the next working day after a person's last day.
cause: Leaver notices reach IT in a weekly email from the people team rather than on the leaving date, and the payments admin console and the customer support tool have their own logins outside single sign-on.
rating: High
raised_by: Internal audit
date_raised: 2026-04-14
scope: Payments admin console; Customer support tool
```

### 3. The agreed action plan (export)

```
promise_id,action_id,action,owner,due_date,promised_evidence,kind,scope,period_from,period_to
P1,A1,Send leaver notices from the HR system to the IT service desk automatically on the leaving date,People operations lead,2026-06-30,Service desk record showing the automatic leaver notice switched on,implementation,all,,
P2,A2,Put the payments admin console and the customer support tool behind single sign-on,IT operations manager,2026-07-31,Change record for each system moved to single sign-on,implementation,,,
P3,A3,Add a monthly leaver access check for both systems to the access control standard and run it,IT operations manager,2026-08-31,Access control standard with the monthly leaver check added,design,,,
P4,A3,Add a monthly leaver access check for both systems to the access control standard and run it,IT operations manager,2026-08-31,Signed monthly leaver access checks for both systems,operation,,2026-08-01,2026-10-31
```

### 4. The owner's response (as received)

```
From: IT operations manager
Date: 2 November 2026

All three actions on IA-2026-07 are complete. The automatic leaver notice
went live on 22 June 2026. Both systems have been on single sign-on since
28 July 2026. The monthly leaver check has run since August and the
sign-offs are attached. Please close the finding.
```

### 5. The evidence list (export)

```
evidence_id,promise_id,description,kind,record_date,covers_from,covers_to,scope,location
E1,P1,Service desk ticket 4471: automatic leaver notice from the HR system switched on,implementation,2026-06-22,,,all,Service desk / ticket 4471
E2,P2,Change record CHG-0912: payments admin console moved to single sign-on,implementation,2026-07-28,,,Payments admin console,Change log / CHG-0912
E3,P3,Access control standard AC-02 revision 4 with section 6 monthly leaver check,design,2026-08-03,,,all,Policy library / AC-02
E4,P4,Monthly leaver access check for August 2026 signed by the IT operations manager,operation,2026-09-02,2026-08-01,2026-08-31,Payments admin console; Customer support tool,IT share / Access checks / 2026
E5,P4,Monthly leaver access check for October 2026 signed by the IT operations manager,operation,2026-11-02,2026-10-01,2026-10-31,Payments admin console; Customer support tool,
E6,P2,Email from the IT operations manager saying the customer support tool moved to single sign-on,statement,2026-07-29,,,Customer support tool,Attached to the response
E7,P3,Access control standard AC-02 revision 3,design,2026-01-15,,,all,Policy library / AC-02
E8,,Screenshot of the single sign-on user list for the payments admin console,implementation,2026-10-30,,,Payments admin console,Attached to the response
```

## The comparison

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

## How the figures were reached

- **Promised items.** The plan has four rows, P1 to P4, across three actions. P1 and P3 each have a counted record and nothing missing. P2 has a counted record for one of its two systems. P4 has counted records for August and October but not September. So 2 + 2 + 0 = 4.
- **Evidence rows.** E1 to E5 pass all four tests: each has a date on or after 14 April 2026 and no later than 4 November 2026, and each is the kind its promise asked for. E6 is a statement against an implementation promise, and E7 is dated 15 January 2026, before the finding was raised. E8 names no promise. So 5 + 2 + 1 = 8.
- **The September gap.** P4 runs from 1 August to 31 October 2026. E4 covers 1 to 31 August and E5 covers 1 to 31 October, which leaves 1 to 30 September uncovered.
- **The plan's reach.** P1 is scoped "all", which reaches both systems in the finding's scope, so no scope item is left out.
