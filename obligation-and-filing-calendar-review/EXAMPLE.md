# Obligation and filing calendar review: an invented example

*Illustrative example with invented data.* The organisation, its companies, its plant, the registries and agencies, the people and every date below are invented. The organisation is an invented maker of industrial coatings, called the Company here, with two companies in its group (Entity A and Entity B) and one plant (Plant 1). The bodies it reports to are named by letter, and people are named by role. The compliance lead runs the quarterly review on Wednesday 11 November 2026. First come the inputs the compliance lead supplied, in full, then the list the workflow template returned.

## The inputs

### 1. Settings (typed by the compliance lead)

```
Organisation: the Company
Today: 2026-11-11
Window: 90 days
Scope: every row
Reviewer: Compliance lead
Default verifying role: Counsel
Re-verification period: 12 months
Current owners: Company secretary, Office manager, Environmental lead, Maintenance manager
```

### 2. Obligation register (exported from the Company's register)

```
obligation_id,obligation,kind,entity_or_site,owed_to,owner,due_date,frequency,evidence_required,verified_by,verified_on
OB-01,Annual report,filing,Entity A,Registry A,Company secretary,2026-12-15,annual,filing receipt,Counsel,2026-03-02
OB-02,Annual report,filing,Entity B,Registry B,Company secretary,2027-01-31,annual,filing receipt,Counsel,2025-06-10
OB-03,Business licence renewal,renewal,Plant 1,City licensing office C,Office manager,2026-12-31,annual,renewed licence,Counsel,2026-02-20
OB-04,Air permit quarterly monitoring report,report,Plant 1,Environmental agency E,Environmental lead,2026-10-30,quarterly,submission confirmation and monitoring log,Environmental specialist,2026-01-15
OB-05,Stormwater sampling,monitoring,Plant 1,Water authority W,,2026-12-20,quarterly,laboratory results and sampling log,Environmental specialist,2026-01-15
OB-06,Hazardous materials inventory report,report,Plant 1,Fire authority F,Environmental lead,2027-03-01,annual,submission confirmation,Environmental specialist,2026-01-15
OB-07,Boiler inspection certificate renewal,renewal,Plant 1,Inspection body I,Maintenance manager,2027-01-15,annual,inspection certificate,,
OB-08,Annual emissions inventory submission,report,Plant 1,Environmental agency E,Environmental lead,2026-09-30,annual,submission confirmation,Environmental specialist,2026-01-15
OB-09,Waste generator registration renewal,renewal,Plant 1,Environmental agency E,Environmental lead,,every two years,renewed registration,Environmental specialist,2026-01-15
OB-10,Annual report for registration in another state,filing,Entity A,Registry S,Controller,2027-02-05,annual,filing receipt,Counsel,2026-04-01
```

### 3. Evidence log

```
evidence_id,obligation_id,for_due_date,evidence_type,location,dated,recorded_by
EV-01,OB-08,2026-09-30,submission confirmation,Compliance drive/Environmental/2026/Emissions,2026-09-24,Environmental lead
EV-02,OB-03,2025-12-31,renewed licence,Compliance drive/Licences/Plant 1/2025,2025-12-12,Office manager
EV-03,OB-02,2027-01-31,filing receipt,Compliance drive/Entities/Entity B/2027,2026-11-05,Company secretary
EV-04,OB-12,2026-10-15,training attendance sheet,Compliance drive/Environmental/Training,2026-10-15,Environmental lead
EV-05,OB-07,2027-01-15,inspection certificate,,2026-11-09,Maintenance manager
```

### 4. Notices received

```
notice_id,received_on,from,about,date_stated,obligation_id
N-1,2026-10-20,Registry A,Annual report reminder for Entity A,2026-11-30,OB-01
N-2,2026-11-02,Water authority W,New annual stormwater report form,2027-01-28,
N-3,2026-11-06,Registry B,Annual report reminder for Entity B,2027-01-31,OB-02
```

## The output

**OBLIGATION AND FILING CALENDAR REVIEW: the Company**

For: Compliance lead. Prepared: Wed 2026-11-11. Window: Wed 2026-11-11 to Tue 2027-02-09 (today plus 90 days, both included). Scope: every row.
From: the obligation register (10 rows, 10 in scope), the evidence log (5 rows), the notices (3 rows) and the settings.
Column check: all headers matched.
Every due date is used exactly as the register records it.
No date has been worked out and no obligation has been added.
In scope: 10. Past recorded due date, no evidence on file: 1. Coming due in the window: 6. Past recorded due date, evidence on file: 1. No usable due date: 1. Due after the window: 1. Questions: 11.

**1. PAST RECORDED DUE DATE, NO EVIDENCE ON FILE**

OB-04 Air permit quarterly monitoring report (report). Plant 1. Owed to: Environmental agency E.
- Owner: Environmental lead.
- Due as recorded: Fri 2026-10-30, 12 days ago. Frequency as recorded: quarterly.
- Evidence required: submission confirmation and monitoring log. Evidence on file: none on file for this due date.
- Verified: Environmental specialist, Thu 2026-01-15.
- Notices: none.
- Gaps: no evidence for a passed due date. See Q1.

**2. COMING DUE IN THE WINDOW**

OB-01 Annual report (filing). Entity A. Owed to: Registry A.
- Owner: Company secretary.
- Due as recorded: Tue 2026-12-15, in 34 days. Frequency as recorded: annual.
- Evidence required: filing receipt. Evidence on file: none on file for this due date.
- Verified: Counsel, Mon 2026-03-02.
- Notices: N-1, received Tue 2026-10-20, states Mon 2026-11-30.
- Gaps: notice states another date. See Q2.

OB-05 Stormwater sampling (monitoring). Plant 1. Owed to: Water authority W.
- Owner: not assigned.
- Due as recorded: Sun 2026-12-20, in 39 days. Frequency as recorded: quarterly.
- Evidence required: laboratory results and sampling log. Evidence on file: none on file for this due date.
- Verified: Environmental specialist, Thu 2026-01-15.
- Notices: none.
- Gaps: no owner. See Q3.

OB-03 Business licence renewal (renewal). Plant 1. Owed to: City licensing office C.
- Owner: Office manager.
- Due as recorded: Thu 2026-12-31, in 50 days. Frequency as recorded: annual.
- Evidence required: renewed licence. Evidence on file: none on file for this due date.
- Verified: Counsel, Fri 2026-02-20.
- Notices: none.
- Gaps: None.

OB-07 Boiler inspection certificate renewal (renewal). Plant 1. Owed to: Inspection body I.
- Owner: Maintenance manager.
- Due as recorded: Fri 2027-01-15, in 65 days. Frequency as recorded: annual.
- Evidence required: inspection certificate. Evidence on file: EV-05, inspection certificate, dated Mon 2026-11-09, at location not given.
- Verified: not recorded.
- Notices: none.
- Gaps: verification not recorded; evidence location not given. See Q4, Q5.

OB-02 Annual report (filing). Entity B. Owed to: Registry B.
- Owner: Company secretary.
- Due as recorded: Sun 2027-01-31, in 81 days. Frequency as recorded: annual.
- Evidence required: filing receipt. Evidence on file: EV-03, filing receipt, dated Thu 2026-11-05, at Compliance drive/Entities/Entity B/2027.
- Verified: Counsel, Tue 2025-06-10, older than the 12-month period.
- Notices: N-3, received Fri 2026-11-06, states Sun 2027-01-31.
- Gaps: verification older than the period. See Q6.

OB-10 Annual report for registration in another state (filing). Entity A. Owed to: Registry S.
- Owner: Controller, not on the current list.
- Due as recorded: Fri 2027-02-05, in 86 days. Frequency as recorded: annual.
- Evidence required: filing receipt. Evidence on file: none on file for this due date.
- Verified: Counsel, Wed 2026-04-01.
- Notices: none.
- Gaps: owner not current. See Q7.

**3. PAST RECORDED DUE DATE, EVIDENCE ON FILE**

OB-08 Annual emissions inventory submission (report). Plant 1. Owed to: Environmental agency E.
- Owner: Environmental lead.
- Due as recorded: Wed 2026-09-30, 42 days ago. Frequency as recorded: annual.
- Evidence required: submission confirmation. Evidence on file: EV-01, submission confirmation, dated Thu 2026-09-24, at Compliance drive/Environmental/2026/Emissions.
- Verified: Environmental specialist, Thu 2026-01-15.
- Notices: none.
- Gaps: next due date not recorded. See Q8.

**4. NO USABLE DUE DATE**

OB-09 Waste generator registration renewal (renewal). Plant 1. Owed to: Environmental agency E.
- Owner: Environmental lead.
- Due as recorded: not recorded. Frequency as recorded: every two years.
- Evidence required: renewed registration. Evidence on file: none on file; no usable due date to match.
- Verified: Environmental specialist, Thu 2026-01-15.
- Notices: none.
- Gaps: no usable due date. See Q9.

**5. NOTICES NOT MATCHING THE REGISTER**

- N-1, received Tue 2026-10-20 from Registry A: Annual report reminder for Entity A. Date stated: Mon 2026-11-30. The register records Tue 2026-12-15 for OB-01; the two differ. See Q2.
- N-2, received Mon 2026-11-02 from Water authority W: New annual stormwater report form. Date stated: Thu 2027-01-28. Not in the register; nothing has been added. See Q10.

**6. EVIDENCE NOT PLACED**

- EV-04: training attendance sheet, for OB-12, dated Thu 2026-10-15, at Compliance drive/Environmental/Training, recorded by Environmental lead. No such obligation in the register. See Q11.

**7. QUESTIONS**

- Q1. Environmental lead (owner). OB-04 Air permit quarterly monitoring report, owed to Environmental agency E: the register records Fri 2026-10-30, 12 days ago, and asks for a submission confirmation and monitoring log; none is on file for that due date. Where is the evidence of completion for that due date?
- Q2. Counsel (verifying role). OB-01 Annual report, Entity A: the register records Tue 2026-12-15; notice N-1 from Registry A, received Tue 2026-10-20, states Mon 2026-11-30. Which date should the register hold?
- Q3. Compliance lead (reviewer). OB-05 Stormwater sampling, Plant 1, recorded as due Sun 2026-12-20: no owner is recorded. Who owns it?
- Q4. Counsel (verifying role). OB-07 Boiler inspection certificate renewal, recorded as due Fri 2027-01-15: the register records no verification. Are the obligation and its due date as recorded?
- Q5. Maintenance manager (owner). OB-07: evidence EV-05, an inspection certificate dated Mon 2026-11-09, has no location. Where is it kept?
- Q6. Counsel (verifying role). OB-02 Annual report, Entity B: last verified Tue 2025-06-10, more than 12 months before today. Are the obligation and its due date of Sun 2027-01-31 still as recorded?
- Q7. Compliance lead (reviewer). OB-10 Annual report for registration in another state, Entity A, recorded as due Fri 2027-02-05: the owner, Controller, is not on the list of current owners. Who owns it now?
- Q8. Environmental specialist (verifying role). OB-08 Annual emissions inventory submission: the register still records Wed 2026-09-30, and EV-01, a submission confirmation dated Thu 2026-09-24, is on file for that date. What next due date should the register hold?
- Q9. Environmental specialist (verifying role). OB-09 Waste generator registration renewal: no due date is recorded, and the frequency is recorded as every two years. What due date should the register hold?
- Q10. Compliance lead (reviewer). N-2 from Water authority W, received Mon 2026-11-02, about a new annual stormwater report form, states Thu 2027-01-28 and names no obligation in the register. Who confirms whether the register should hold an entry for it?
- Q11. Environmental lead (recorded by). EV-04, a training attendance sheet dated Thu 2026-10-15, is recorded for OB-12, which is not in the register. Which obligation is it evidence for?

**8. ALSO NOTED**

- Due after the window: OB-06, Mon 2027-03-01.
- Evidence for another due date: EV-02 for OB-03, for Wed 2025-12-31.
- Notices that agree with the register: N-3 for OB-02.

Draft for the Compliance lead. Nothing has been filed, submitted, paid, sent, marked complete or changed in the register.
