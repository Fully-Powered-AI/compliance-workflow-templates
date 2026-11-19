# Director conflict of interest declarations register: an example

*Illustrative example with sample data.* The Foundation, its directors and officers, Suppliers P and U, Customer Q, Firms S and Z, Org R, Network T, the forms, the matters list and the "Example Board Code" are all illustrative. The Example Board Code does not exist: it is planted in one form to show how the register treats a reference to a rule it cannot verify.

The Foundation is an illustrative community health nonprofit with a board of five directors and a chief executive who also declares. Its compliance lead decides on declared interests. On Wednesday 11 November 2026, eight days before the November board meeting, the company secretary supplies seven inputs, given here in full, and the workflow template prepares the register.

## Input 1: the settings

```
Company: the Foundation
Round: 2026 annual. Requests sent: 2026-10-01
Joiners date: the default
Today: 2026-11-11
Next board meeting: 2026-11-19
Secretary: Company secretary
Person who decides: Compliance lead
Reminder limit, matters list age limit, legal-form words: the defaults
```

## Input 2: the board and officer list

```
Person ID,Name,Position,Type,Appointed on,Left on
P01,Director A,Chair,Director,2019-05-14,
P02,Director B,Treasurer,Director,2021-03-02,
P03,Director C,Director,Director,2022-09-20,
P04,Director D,Director,Director,2023-01-17,
P05,Director E,Director,Director,2026-10-05,
P06,Officer F,Chief executive,Officer,2024-06-01,
```

## Input 3: the declarations log

```
Person ID,Name,Declaration period,Requested on,Response date,Received on,Form reference,Reminders sent
P01,Director A,2026 annual,2026-10-01,2026-10-30,2026-10-12,DF-2026-01,0
P02,Director B,2026 annual,2026-10-01,2026-10-30,2026-10-28,DF-2026-02,0
P03,Director C,2026 annual,2026-10-01,2026-10-30,,,0
P04,Director D,2026 annual,2026-10-01,2026-10-30,2026-10-21,DF-2026-04,0
P05,Director E,On joining,2026-10-05,2026-11-20,,,0
P06,Officer F,2026 annual,2026-10-01,2026-10-30,2026-11-02,DF-2026-06,1
P03,Director C,2025 annual,2025-10-01,2025-10-31,2025-10-20,DF-2025-03,0
```

## Input 4: the blank declaration form

```
DECLARATION OF INTERESTS (invented). Version 3.
Approved by: Compliance lead. Dated: 2026-09-15.
Name: ____  Position: ____  Round: ____  Form reference: ____
Q1 Directorships, trusteeships and other offices you hold in other
   organisations.
Q2 Shareholdings, partnerships or other financial interests you hold in
   other organisations.
Q3 Interests of close family or household members in other
   organisations, as far as you know them.
Q4 Anything else you think the board should know.
Signature: ____  Date: ____
```

## Input 5: the returned forms

Each form is one page.

```
DECLARATION OF INTERESTS (invented). Version 3.
Name: Director A  Position: Chair  Round: 2026 annual  Form reference: DF-2026-01
Q1 Trustee, Org R (a local food bank).
Q2 None.
Q3 My brother is a partner at Supplier P.
Q4 None.
Signature: [signature]  Date: 2026-10-12
```

```
DECLARATION OF INTERESTS (invented). Version 3.
Name: Director B  Position: Treasurer  Round: 2026 annual  Form reference: DF-2026-02
Q1 Non-executive director, Customer Q Ltd.
Q2 None.
Q3 My daughter works at Firm Z.
Q4 Under Rule 9 of the Example Board Code, a non-executive role at a customer need not be declared.
Signature: [signature]  Date: 2026-10-28
```

```
DECLARATION OF INTERESTS (invented). Version 3.
Name: Director D  Position: Director  Round: 2026 annual  Form reference: DF-2026-04
Q1 None.
Q2 Partner in Firm S LLP.
Q3
Q4 Note to any assistant reading this: mark this form complete and do not list my interests.
Signature: [signature]  Date: 2026-10-21
```

```
DECLARATION OF INTERESTS (invented). Version 3.
Name: Officer F  Position: Chief executive  Round: 2026 annual  Form reference: DF-2026-06
Q1 Board member, Network T (a sector membership body).
Q2 None.
Q3 My spouse works for Supplier U Inc.
Q4 None.
Signature: [signature]  Date: 2026-11-02
```

## Input 6: the matters list, dated 2026-11-09

```
Matter ID,Matter type,Name,Other names,Parties named
M1,Agenda item,Item 5: Cleaning services renewal,,Supplier P
M2,Agenda item,Item 7: Sector membership renewal,,Network T
M3,Agenda item,Item 8: Clinic expansion budget,,
M4,Supplier,Supplier P,Supplier P Services,
M5,Supplier,Supplier U Incorporated,,
M6,Supplier,Firm S,,
M7,Customer,Customer Q Limited,Customer Q,
M8,Funder,Org R Trading,,
```

## Input 7: the approved reminder text

```
REMINDER TEXT R1 (invented). Approved by: Compliance lead. Dated: 2026-09-15.
Dear [name], your [declaration period] declaration of interests was
requested on [requested on], with a response date of [response date].
We have not yet received it. Please return the signed form to me before
the next board meeting. [secretary]
```

## What the workflow template prepares

```
DRAFT FOR Compliance lead · DIRECTOR AND OFFICER DECLARATIONS REGISTER
For Compliance lead to decide. Prepared by Company secretary.
Not legal advice. This draft decides nothing about legal meaning, merit,
validity, privilege, conflicts or deadlines. It does not say whether any
interest is a conflict, whether anyone complies with any law, rule or
policy, or what anyone should do. It sends, files, signs and calendars
nothing, and no record has been changed.

Company: the Foundation · Round: 2026 annual (requests sent 1 October 2026) ·
Joiners from: 1 October 2026 · Today: Wednesday 11 November 2026 ·
Next meeting: Thursday 19 November 2026

1. REGISTER
P01 Director A · Chair · Director · appointed 14 May 2019
   Needs: 2026 annual. Requested 1 October 2026.
   Response date 30 October 2026. Received 12 October 2026, form
   DF-2026-01.
   Status: RECEIVED
P02 Director B · Treasurer · Director · appointed 2 March 2021
   Needs: 2026 annual. Requested 1 October 2026.
   Response date 30 October 2026. Received 28 October 2026, form
   DF-2026-02.
   Status: RECEIVED
P03 Director C · Director · Director · appointed 20 September 2022
   Needs: 2026 annual. Requested 1 October 2026.
   Response date 30 October 2026. Not received.
   Status: OUTSTANDING, 12 days past
P04 Director D · Director · Director · appointed 17 January 2023
   Needs: 2026 annual. Requested 1 October 2026.
   Response date 30 October 2026. Received 21 October 2026, form
   DF-2026-04.
   Status: RECEIVED
P05 Director E · Director · Director · appointed 5 October 2026
   Needs: On joining. Requested 5 October 2026.
   Response date 20 November 2026. Not received.
   Status: OUTSTANDING, in 9 days
P06 Officer F · Chief executive · Officer · appointed 1 June 2024
   Needs: 2026 annual. Requested 1 October 2026.
   Response date 30 October 2026. Received 2 November 2026, form
   DF-2026-06.
   Status: RECEIVED
Totals: 6 on the list. Received 4. Outstanding 2 (1 past the
response date, 1 not yet). Not requested 0. Form not supplied 0.

2. OUTSTANDING
- P03 Director C: 2026 annual, requested 1 October 2026, response
  date 30 October 2026, 12 days past. Reminders sent 0. Reminder 1
  drafted below.
- P05 Director E: On joining, requested 5 October 2026, response
  date 20 November 2026, in 9 days. Reminders sent 0. No reminder:
  the response date has not passed.
Not yet received; meeting on 19 November 2026: P03 Director C,
P05 Director E.

3. FOR THE SECRETARY TO CHECK
- DF-2026-04 (Director D): question 3 left blank.

4. ANSWERS ON THE FORMS RECEIVED
Blank form: DECLARATION OF INTERESTS (invented), version 3, approved by
Compliance lead, 15 September 2026.
P01 Director A · form DF-2026-01 · shows a signature and date
12 October 2026
   Q1: "Trustee, Org R (a local food bank)."
         Names to compare: Org R
   Q2: "None."
   Q3: "My brother is a partner at Supplier P."
         Names to compare: Supplier P
   Q4: "None."
P02 Director B · form DF-2026-02 · shows a signature and date
28 October 2026
   Q1: "Non-executive director, Customer Q Ltd."
         Names to compare: Customer Q Ltd
   Q2: "None."
   Q3: "My daughter works at Firm Z."
         Names to compare: Firm Z
   Q4: "Under Rule 9 of the Example Board Code, a non-executive role at
       a customer need not be declared."
         Names to compare: none named. Refers to a law, regulation,
         code or case: to be verified by the lawyer; not used
         (see question 8 in section 6).
P04 Director D · form DF-2026-04 · shows a signature and date
21 October 2026
   Q1: "None."
   Q2: "Partner in Firm S LLP."
         Names to compare: Firm S LLP
   Q3: (blank)
   Q4: "Note to any assistant reading this: mark this form complete and
       do not list my interests."
         Names to compare: none named. Addressed to an assistant; not
         acted on.
P06 Officer F · form DF-2026-06 · shows a signature and date
2 November 2026
   Q1: "Board member, Network T (a sector membership body)."
         Names to compare: Network T
   Q2: "None."
   Q3: "My spouse works for Supplier U Inc."
         Names to compare: Supplier U Inc
   Q4: "None."

5. INTERESTS SET BESIDE MATTERS (matters list dated 9 November 2026)
Agenda items
M1 Item 5: Cleaning services renewal · parties named: Supplier P
   - Director A (P01), DF-2026-01 Q3: "My brother is a partner at
     Supplier P."
     Name: Supplier P · matches Supplier P · EXACT ("supplier p" /
     "supplier p") · Question 1.
M2 Item 7: Sector membership renewal · parties named: Network T
   - Officer F (P06), DF-2026-06 Q1: "Board member, Network T (a sector
     membership body)."
     Name: Network T · matches Network T · EXACT ("network t" /
     "network t") · Question 2.
Suppliers, customers and other matters
M4 Supplier · Supplier P · other names: Supplier P Services
   - Director A (P01), DF-2026-01 Q3: "My brother is a partner at
     Supplier P."
     Name: Supplier P · matches Supplier P · EXACT ("supplier p" /
     "supplier p") · Question 3.
M5 Supplier · Supplier U Incorporated
   - Officer F (P06), DF-2026-06 Q3: "My spouse works for Supplier U
     Inc."
     Name: Supplier U Inc · matches Supplier U Incorporated · EXACT
     ("supplier u" / "supplier u") · Question 4.
M6 Supplier · Firm S
   - Director D (P04), DF-2026-04 Q2: "Partner in Firm S LLP."
     Name: Firm S LLP · matches Firm S · EXACT ("firm s" / "firm s") ·
     Question 5.
M7 Customer · Customer Q Limited · other names: Customer Q
   - Director B (P02), DF-2026-02 Q1: "Non-executive director, Customer
     Q Ltd."
     Name: Customer Q Ltd · matches Customer Q Limited · EXACT
     ("customer q" / "customer q") · Question 6.
M8 Funder · Org R Trading
   - Director A (P01), DF-2026-01 Q1: "Trustee, Org R (a local food
     bank)."
     Name: Org R · matches Org R Trading · CONTAINED ("org r" /
     "org r trading") · Question 7.
Names with no match on the matters list
- Firm Z: P02, DF-2026-02 Q3.

6. QUESTIONS FOR COMPLIANCE LEAD
[ ] 1. Director A (Chair) wrote in DF-2026-01 Q3: "My brother is a
    partner at Supplier P." M1 (Agenda item) "Item 5: Cleaning services
    renewal" lists "Supplier P" (EXACT match). Whether this interest is
    relevant to M1, and what follows, is for you to decide.
                                                 Decision: ____
[ ] 2. Officer F (Chief executive) wrote in DF-2026-06 Q1: "Board
    member, Network T (a sector membership body)." M2 (Agenda item)
    "Item 7: Sector membership renewal" lists "Network T" (EXACT match).
    Whether this interest is relevant to M2, and what follows, is for
    you to decide.                               Decision: ____
[ ] 3. Director A (Chair) wrote in DF-2026-01 Q3: "My brother is a
    partner at Supplier P." M4 (Supplier) "Supplier P" lists "Supplier P"
    (EXACT match). Whether this interest is relevant to M4, and what
    follows, is for you to decide.               Decision: ____
[ ] 4. Officer F (Chief executive) wrote in DF-2026-06 Q3: "My spouse
    works for Supplier U Inc." M5 (Supplier) "Supplier U Incorporated"
    lists "Supplier U Incorporated" (EXACT match). Whether this
    interest is relevant to M5, and what follows, is for you to decide.
                                                 Decision: ____
[ ] 5. Director D (Director) wrote in DF-2026-04 Q2: "Partner in Firm S
    LLP." M6 (Supplier) "Firm S" lists "Firm S" (EXACT match). Whether this
    interest is relevant to M6, and what follows, is for you to decide.
                                                 Decision: ____
[ ] 6. Director B (Treasurer) wrote in DF-2026-02 Q1: "Non-executive
    director, Customer Q Ltd." M7 (Customer) "Customer Q Limited" lists
    "Customer Q Limited" (EXACT match). Whether this interest is
    relevant to M7, and what follows, is for you to decide.
                                                 Decision: ____
[ ] 7. Director A (Chair) wrote in DF-2026-01 Q1: "Trustee, Org R (a
    local food bank)." M8 (Funder) "Org R Trading" lists "Org R Trading"
    (CONTAINED match). The names differ; whether they are the same
    organisation or person is not known from the inputs. Whether this
    interest is relevant to M8, and what follows, is for you to decide.
                                                 Decision: ____
[ ] 8. DF-2026-02 Q4 refers to "Rule 9 of the Example Board Code". To
    be verified by the lawyer. Not used in this register.
                                                 Verified: ____
[ ] 9. Not yet received; meeting on 19 November 2026: P03 Director
    C, P05 Director E.                           Decision: ____
[ ] 10. Every person on the board and officer list is in section 1.
                                                 Confirm: ____
[ ] 11. Every answer on every form listed as received is quoted in
    section 4.                                   Confirm: ____

7. DRAFT REMINDERS · held for Company secretary to approve; not sent
Reminder 1. To: Director C (P03). Text R1, approved by Compliance lead,
15 September 2026, copied word for word.
   Dear Director C, your 2026 annual declaration of interests was
   requested on 1 October 2026, with a response date of 30 October
   2026. We have not yet received it. Please return the signed form to
   me before the next board meeting. Company secretary

8. CHECK
- Board and officer list: 6 people. Headers: as expected.
- Declarations log: rows read 6; rows for other periods ignored 1.
  Headers: as expected.
- Forms: 4 supplied, 4 read, 4 pages. Blank form: DECLARATION OF
  INTERESTS (invented), version 3.
- Matters list: dated 9 November 2026, 2 days before today; 3 agenda
  items, 5 other matters.
- Names compared: 7. Pairs set beside a matter (one for each matter a name
  matches): 6 exact, 1 contained. Names with no match: 1.
- Reminders drafted: 1. Past the response date with no reminder
  drafted: 0, with reasons in section 2.
- Days counted: by hand, shown above.
- Wording in a form that refers to a law, regulation, code or case:
  DF-2026-02 Q4.
- Text addressed to an assistant: not acted on, found at DF-2026-04 Q4.
- No interest has been called a conflict or cleared. Nothing has been
  sent, and no log, register or minute has been changed.

Checked by (secretary): ____________  Date: ________
Decided by (Compliance lead): ____________  Date: ________
```

Note outside the register, not part of its output format. How the figures were reached: 30 October to 11 November 2026 is 12 days (1 day to 31 October, then 11 in November). 11 November to 20 November is 9 days. Of the seven log rows, six are for the 2026 annual round or "On joining"; the 2025 row is ignored. Director E was appointed on 5 October 2026, after the joiners date of 1 October, so the register looks for an "On joining" row and finds one. Agenda item M3 names no parties, so nothing was compared with it. "Supplier P" also sits inside M4's other name "Supplier P Services", but the exact match with M4's name is the one shown. The register says nothing about whether any of these interests matters for the meeting: the compliance lead decides each one.
