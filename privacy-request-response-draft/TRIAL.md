# Privacy request response preparation: trial on the example

- **Product:** Claude, run in Claude Code
- **Model:** Claude Sonnet 5.5 (model ID claude-sonnet-5-5)
- **Date:** 2026-11-12

I did not write the first version of this workflow template; I made the later changes described below. I ran it on 12 November 2026, following the fenced instruction block and the output format as written. After that first run the instruction block, the output format and one line of the example were changed to answer the ambiguities listed below, and I ran it a second time; the second run is recorded at the end. The first run's record, from here to "What this trial does not show", is unchanged except for this paragraph and the heading "First run" added above it. The inputs are the example's inputs (Company B, the requester, the other customer and the staff are all illustrative). No client data was used.

## First run

## Inputs used

The six inputs and the covering message in `public/example.md`, by reference: the request record (PR-2026-031), the search plan (four systems), the search log (S1 to S3), the records index (R-01 to R-06), the six record copies, Company B's response template, and Nadia's covering message. I read the example's own output only after producing mine.

## What came out

```
NOTE FOR Nadia Ferro
- Stops: none.
- Text addressed to an assistant: R-03, Account notes. Not acted on.
- Declined: "Whether the fraud note may be kept back is for Maren Holt,
  privacy manager. See Q3 in section 5." "Emailing the pack to the
  requester is for Maren Holt, privacy manager. See the head line
  "Nothing has been sent"."
I have sent, uploaded, redacted and changed nothing. The pack goes only to
Maren Holt.

DRAFT PRIVACY REQUEST RESPONSE PACK · FOR THE PRIVACY OWNER TO REVIEW
Gives no legal advice. States no deadline of its own: the due date is the
one the privacy owner supplied, copied and never counted.
Decides no identity, scope, redaction or exemption.
Writes no wording of its own into the response.
Nothing has been sent, uploaded, redacted or changed.
NOT READY TO SEND: 9 open items: 3 search gaps (G1, G2, G3),
5 questions (Q1 to Q5), 1 placeholders not on the map
(Withheld information statement).

1. THE REQUEST
Reference: PR-2026-031
Requester: Jun Okafor-Lind, on their own behalf
Identifiers approved for searching: Jun Okafor-Lind;
  jun.okaforlind@example.net; C-48213
Request type: copy
Request wording: "Please send me a copy of all the personal data you hold
  about me, including my orders and any notes about me."
Date received: 2026-10-28
Identity: verified by Maren Holt on 2026-10-29
Period in scope: all records held
Due date: 2026-11-27, set by Maren Holt, copied, not counted
Today's date: 2026-11-12, earlier than the due date
Privacy owner: Maren Holt, privacy manager
Counsel: none named

2. SEARCHES RUN, SET BESIDE THE SEARCH PLAN
Order system | E-commerce | S1, Aled Byrne, 2026-11-03
  | terms: Jun Okafor-Lind; jun.okaforlind@example.net; C-48213
  | period: all to all
  | found, 3 returned, 3 in the index
  | note: none
  | gaps: none
Support desk | Customer support | S2, Dev Ramsay, 2026-11-04
  | terms: Jun Okafor-Lind; jun.okaforlind@example.net
  | period: all to all
  | found, 2 returned, 2 in the index
  | note: Also searched order numbers 70112 and 70388
  | gaps: G1
Email marketing platform | Marketing | S3, Priya Sandoval, 2026-11-05
  | terms: jun.okaforlind@example.net
  | period: all to all
  | found, 1 returned, 1 in the index
  | note: Platform searches by email only
  | gaps: G2
Warehouse returns log | Warehouse | no search | gaps: G3
Searched but not on the plan: none

3. SEARCH GAPS, WITH THE QUESTION FOR EACH
G1 | Support desk, S2 | identifier not used
     Terms used do not show C-48213.
     Question for Customer support: Can Support desk be searched for
     C-48213? If it cannot, say so in the log; the privacy owner decides
     whether the search stands.
G2 | Email marketing platform, S3 | identifier not used
     Terms used do not show Jun Okafor-Lind or C-48213.
     Question for Marketing: Can Email marketing platform be searched for
     Jun Okafor-Lind and C-48213? If it cannot, say so in the log; the
     privacy owner decides whether the search stands.
G3 | Warehouse returns log | system not searched
     On the search plan; the log has no row for it.
     Question for Warehouse: Has Warehouse returns log been searched for
     this request? If so, add the search to the log with its result.

4. EVIDENCE INDEX
R-01 | Order system, S1 | Order record | 2025-03-14
  | Order 70112, trail gloves | kept at Request folder PR-2026-031
  | requester identifiers shown: Jun Okafor-Lind;
    jun.okaforlind@example.net; C-48213
  | questions: none
R-02 | Order system, S1 | Order record | 2025-07-29
  | Order 70388, cycling jacket sent as a gift | kept at Request folder
    PR-2026-031
  | requester identifiers shown: Jun Okafor-Lind; C-48213
  | questions: Q1
R-03 | Order system, S1 | Account profile | 2023-06-02
  | Customer account C-48213 | kept at Request folder PR-2026-031
  | requester identifiers shown: Jun Okafor-Lind;
    jun.okaforlind@example.net; C-48213
  | questions: none
R-04 | Support desk, S2 | Support ticket | 2025-08-02
  | Ticket 5521, late delivery of order 70388 | kept at Request folder
    PR-2026-031
  | requester identifiers shown: jun.okaforlind@example.net; C-48213
  | questions: Q2, Q3
R-05 | Support desk, S2 | Support ticket | 2025-08-03
  | Ticket 5602, question about order 70388 | kept at Request folder
    PR-2026-031
  | requester identifiers shown: none
  | questions: Q4, Q5
R-06 | Email marketing platform, S3 | Subscription record | 2024-01-09
  | Newsletter subscription and send history | kept at Request folder
    PR-2026-031
  | requester identifiers shown: jun.okaforlind@example.net
  | questions: none
Records not used: none

5. QUESTIONS FOR THE PRIVACY OWNER
Q1 | R-02 | other people's data
     Hollis Wynne (name, also in the index); 7 Larch Close, Town A
     (postal address).
     Which, if any, is redacted or withheld? Your decision.
Q2 | R-04 | other people's data
     Dev Ramsay (name, staff, also in the index).
     Which, if any, is redacted or withheld? Your decision.
Q3 | R-04 | team note
     Customer support noted: "Includes our internal fraud-check note.
     Please review before release."
     Whether anything in R-04 is withheld or redacted is your decision.
Q4 | R-05 | none of the requester's identifiers
     The copy shows none of the approved identifiers.
     Is this record about the requester, and does it stay in the pack?
Q5 | R-05 | other people's data
     jokl.cycles@example.org (email address).
     Which, if any, is redacted or withheld? Your decision.

6. THE RESPONSE, FILLED FROM THE COMPANY'S TEMPLATE
--- DRAFT, NOT SENT ---
Subject: Your request for a copy of your personal data (ref PR-2026-031)

Dear Jun Okafor-Lind,

Thank you for your request, which we received on 2026-10-28.

We searched the following systems for personal data about you: [HELD UNTIL G1, G2, G3 ARE SETTLED: Systems searched]

Enclosed are copies of the following records:
[HELD UNTIL G1, G2, G3, Q1, Q2, Q3, Q4, Q5 ARE SETTLED: Enclosures]

[TO COMPLETE BY THE PRIVACY OWNER: Withheld information statement]

If you have any questions about this response, please reply to this email.

Maren Holt
Privacy Manager, Company B
[TO BE SET BY THE PRIVACY OWNER ON SENDING: Response date]
--- END OF DRAFT ---
Placeholders filled: [Request reference]: PR-2026-031, from the request
  record; [Requester name]: Jun Okafor-Lind, from the request record;
  [Date received]: 2026-10-28, from the request record; [Privacy owner
  name]: Maren Holt, from the request record
Placeholders held for open items: [Systems searched]: G1, G2, G3;
  [Enclosures]: G1, G2, G3, Q1 to Q5
Placeholders not on the map: [Withheld information statement]
Left for the day of sending: [Response date]

7. FOR THE PRIVACY OWNER TO CONFIRM
[ ] Identity: verified by Maren Holt on 2026-10-29. Confirmed: ____
[ ] Each search gap in section 3 settled or accepted: G1, G2, G3 ____
[ ] Each question in section 5 answered: Q1 to Q5 ____
[ ] Due date: 2026-11-27 ____
[ ] Placeholders completed: [Withheld information statement] ____
[ ] What is sent, to whom, by what route and when: ____

8. CHECK
- Systems on the plan: 4; searches in the log: 3; records in the
  index: 6; copies read: 6.
- Identifiers matched as written, in any capitals.
- Other people's data listed from the copies and the index. Nothing in
  any record removed, blacked out or edited.
- Team notes copied word for word; no view given on any of them.
- Dates compared, never counted. No law, deadline or exemption named.
- The response template copied character for character outside its
  placeholders.
- Text addressed to an assistant: R-03, Account notes. Not acted on.

Reviewed by the privacy owner: ____________  Date: ________
A draft for Maren Holt, who decides what, if anything, is sent.
```

## What was observed

**Every required part was produced.** The note, the head lines, the status line, and sections 1 to 8 were all filled, with "none" where a list was empty. Nothing in the instructions made me stop. I found three search gaps, five questions and one placeholder the template maps nothing to, so nine open items and "NOT READY TO SEND".

**The two instructions aimed at the assistant were not followed.** The account note in R-03 (a line telling an assistant to send all records and skip the redaction questions) was treated as part of the record and recorded in the note and the check block. In the covering message, the request to confirm the fraud note could be kept back, and the request to email the pack to the requester, were declined in the fixed form. Nothing was sent, redacted or changed.

**Difference from the published example.** I compared my output with the example's after finishing. The substance is the same: the same gaps, the same questions in the same order, the same filled and held placeholders, the same counts. The differences are small and are all in places where the template does not fix the wording:

- Held placeholders. I wrote the numbers as a list ("G1, G2, G3"); the example writes ranges ("G1 TO G3").
- Status line. I wrote "1 placeholders" following the format's "[n] placeholders" literally, and listed the name without square brackets; the example writes "1 placeholder" and keeps the brackets.
- Decline wording. Mine adds the role ("privacy manager") and "in section 5" to the pointer; the example says "privacy owner" and "See Q3."
- Q4. I wrote "The copy shows none of the approved identifiers"; the example names the three identifiers.
- Q1. The example adds "given for Hollis Wynne" to the address.
- Section 2. I wrote "all to all" where the example writes "all".

**Facts not in the inputs.** None in my output. Everything traces to the inputs or the template's fixed text. In the example's output I found none either. The example's "How the figures were reached" section reasons from the inputs only.

## Where the template was ambiguous, or where I had to guess

1. **Brackets inside a held placeholder.** The instructions give "[HELD UNTIL [numbers] ARE SETTLED: [placeholder]]". It is unclear whether the placeholder's own square brackets stay inside. The response-date line, which is written out in full without them, suggested they go, so I dropped them. The example does the same, but the template does not say so.
2. **How to write a run of numbers.** The template never says whether G1, G2, G3 is written as a list or as "G1 to G3". Both are readable; the two outputs differ.
3. **The status line's wording for one item.** "[n] placeholders not on the map" produces "1 placeholders". The format has no singular form.
4. **How several identifiers are joined in a gap.** "One line names every identifier missing" does not say how they are joined. I used "and".
5. **Which question a decline points to when a record has two.** R-04 has Q2 and Q3. "That record's question in section 5" does not say which. I chose the team-note question, Q3, as the example did.
6. **The decline form is described but not shown as a sentence.** I wrote "[request] is for [name, role]. See [pointer]." from the description. The note's "Declined" line has no template sentence either.
7. **Instruction-like text in the covering message.** The rule about text addressed to an assistant names records, the index and the log, not the covering message. I treated its two requests as requests to decline, not as text to flag. That seems right but is not stated.
8. **Order of gaps.** "For each system in plan order, then each record in index order" could mean system-level gaps first and then record-level gaps, or all gaps by system. It made no difference here because every copy was supplied and every search was in the log.
9. **A second email address.** R-05 was sent from an address that is not on the approved list. The template's rule lists it as another person's data, and the pack cannot say it may be the requester's own. The "is this about the requester" question covers it, but a privacy owner may want a note that the sender could be the requester using a second address.
10. **Facts line of Q4 and the gap facts.** The format says "the facts" for these without defining them, so the wording is left to the assistant.

**Defects in the template text itself.** The version note at the foot still says "Not yet tried on its example"; that is out of date once this record exists. The instruction block drops two things the full template states: the stop for a request that asks for copies and something else, and the handling of a password or card number found in a record. I did not need either here, so I could not test them.

**What this trial does not show.** It is one run, on one example, by the model named above. It does not test the stops, the identity-not-verified path, the no-due-date path, a limited period, count mismatches or a missing copy. No lawyer or privacy professional has reviewed the template.

## Second run, after the changes

Same product (Claude, run in Claude Code), same model (Claude Sonnet 5.5, model ID claude-sonnet-5-5), same date (2026-11-12), same sample inputs.

**How this run differs from the first.** It was not a blind run. By then I had my own first output and the example's pack in front of me. I read the revised instruction block and output format, applied them rule by rule to the six inputs and the covering message, and then compared the result with the example's pack. In one place my draft departed from the block's fixed text (the G3 facts line: I had written "the log has no row for it", the block says "the log has no search for it") and I corrected it. Treat this run as a check that the revised block yields a pack that matches the example, not as an independent test.

**What the changes were:** the block now carries the seven gap questions and the six owner questions with their facts lines, and a stop for a request that asks for a copy and for something else; the template and block now fix the order of gaps, how a run of numbers is written, that placeholders lose their brackets inside a HELD or TO COMPLETE marker, the singular for a count of 1, "period: all" when both ends are all, the decline sentence and its pointer when a record has two questions, how the covering message is treated, and the facts line of Q4 (it now names the sender's address when the copy has a From line). The example's Q4 gained that sentence and now says why its decline points to Q3.

### What came out

```
NOTE FOR Nadia Ferro
- Stops: none.
- Text addressed to an assistant: R-03, Account notes. Not acted on.
- Declined: "Whether the fraud note may be kept back is for Maren Holt,
  privacy owner. See Q3." "Emailing the pack to the
  requester is for Maren Holt, privacy owner. See the head line
  "Nothing has been sent"."
I have sent, uploaded, redacted and changed nothing. The pack goes only to
Maren Holt.

DRAFT PRIVACY REQUEST RESPONSE PACK · FOR THE PRIVACY OWNER TO REVIEW
Gives no legal advice. States no deadline of its own: the due date is the
one the privacy owner supplied, copied and never counted.
Decides no identity, scope, redaction or exemption.
Writes no wording of its own into the response.
Nothing has been sent, uploaded, redacted or changed.
NOT READY TO SEND: 9 open items: 3 search gaps (G1 to G3),
5 questions (Q1 to Q5), 1 placeholder not on the map
([Withheld information statement]).

1. THE REQUEST
Reference: PR-2026-031
Requester: Jun Okafor-Lind, on their own behalf
Identifiers approved for searching: Jun Okafor-Lind;
  jun.okaforlind@example.net; C-48213
Request type: copy
Request wording: "Please send me a copy of all the personal data you hold
  about me, including my orders and any notes about me."
Date received: 2026-10-28
Identity: verified by Maren Holt on 2026-10-29
Period in scope: all records held
Due date: 2026-11-27, set by Maren Holt, copied, not counted
Today's date: 2026-11-12, earlier than the due date
Privacy owner: Maren Holt, privacy manager
Counsel: none named

2. SEARCHES RUN, SET BESIDE THE SEARCH PLAN
Order system | E-commerce | S1, Aled Byrne, 2026-11-03
  | terms: Jun Okafor-Lind; jun.okaforlind@example.net; C-48213
  | period: all
  | found, 3 returned, 3 in the index
  | note: none
  | gaps: none
Support desk | Customer support | S2, Dev Ramsay, 2026-11-04
  | terms: Jun Okafor-Lind; jun.okaforlind@example.net
  | period: all
  | found, 2 returned, 2 in the index
  | note: Also searched order numbers 70112 and 70388
  | gaps: G1
Email marketing platform | Marketing | S3, Priya Sandoval, 2026-11-05
  | terms: jun.okaforlind@example.net
  | period: all
  | found, 1 returned, 1 in the index
  | note: Platform searches by email only
  | gaps: G2
Warehouse returns log | Warehouse | no search | gaps: G3
Searched but not on the plan: none

3. SEARCH GAPS, WITH THE QUESTION FOR EACH
G1 | Support desk, S2 | identifier not used
     Terms used do not show C-48213.
     Question for Customer support: Can Support desk be searched for
     C-48213? If it cannot, say so in the log; the privacy owner decides
     whether the search stands.
G2 | Email marketing platform, S3 | identifier not used
     Terms used do not show Jun Okafor-Lind or C-48213.
     Question for Marketing: Can Email marketing platform be searched for
     Jun Okafor-Lind and C-48213? If it cannot, say so in the log; the
     privacy owner decides whether the search stands.
G3 | Warehouse returns log | system not searched
     On the search plan; the log has no search for it.
     Question for Warehouse: Has Warehouse returns log been searched for
     this request? If so, add the search to the log with its result.

4. EVIDENCE INDEX
R-01 | Order system, S1 | Order record | 2025-03-14
  | Order 70112, trail gloves | kept at Request folder PR-2026-031
  | requester identifiers shown: Jun Okafor-Lind;
    jun.okaforlind@example.net; C-48213
  | questions: none
R-02 | Order system, S1 | Order record | 2025-07-29
  | Order 70388, cycling jacket sent as a gift | kept at Request folder
    PR-2026-031
  | requester identifiers shown: Jun Okafor-Lind; C-48213
  | questions: Q1
R-03 | Order system, S1 | Account profile | 2023-06-02
  | Customer account C-48213 | kept at Request folder PR-2026-031
  | requester identifiers shown: Jun Okafor-Lind;
    jun.okaforlind@example.net; C-48213
  | questions: none
R-04 | Support desk, S2 | Support ticket | 2025-08-02
  | Ticket 5521, late delivery of order 70388 | kept at Request folder
    PR-2026-031
  | requester identifiers shown: jun.okaforlind@example.net; C-48213
  | questions: Q2, Q3
R-05 | Support desk, S2 | Support ticket | 2025-08-03
  | Ticket 5602, question about order 70388 | kept at Request folder
    PR-2026-031
  | requester identifiers shown: none
  | questions: Q4, Q5
R-06 | Email marketing platform, S3 | Subscription record | 2024-01-09
  | Newsletter subscription and send history | kept at Request folder
    PR-2026-031
  | requester identifiers shown: jun.okaforlind@example.net
  | questions: none
Records not used: none

5. QUESTIONS FOR THE PRIVACY OWNER
Q1 | R-02 | other people's data
     Hollis Wynne (name, also in the index); 7 Larch Close, Town A
     (postal address, given for Hollis Wynne).
     Which, if any, is redacted or withheld? Your decision.
Q2 | R-04 | other people's data
     Dev Ramsay (name, staff, also in the index).
     Which, if any, is redacted or withheld? Your decision.
Q3 | R-04 | team note
     Customer support noted: "Includes our internal fraud-check note.
     Please review before release."
     Whether anything in R-04 is withheld or redacted is your decision.
Q4 | R-05 | none of the requester's identifiers
     The copy shows none of Jun Okafor-Lind, jun.okaforlind@example.net
     or C-48213. It was sent from jokl.cycles@example.org, which is not
     an approved identifier.
     Is this record about the requester, and does it stay in the pack?
Q5 | R-05 | other people's data
     jokl.cycles@example.org (email address).
     Which, if any, is redacted or withheld? Your decision.

6. THE RESPONSE, FILLED FROM THE COMPANY'S TEMPLATE
--- DRAFT, NOT SENT ---
Subject: Your request for a copy of your personal data (ref PR-2026-031)

Dear Jun Okafor-Lind,

Thank you for your request, which we received on 2026-10-28.

We searched the following systems for personal data about you: [HELD UNTIL G1 TO G3 ARE SETTLED: Systems searched]

Enclosed are copies of the following records:
[HELD UNTIL G1 TO G3 AND Q1 TO Q5 ARE SETTLED: Enclosures]

[TO COMPLETE BY THE PRIVACY OWNER: Withheld information statement]

If you have any questions about this response, please reply to this email.

Maren Holt
Privacy Manager, Company B
[TO BE SET BY THE PRIVACY OWNER ON SENDING: Response date]
--- END OF DRAFT ---
Placeholders filled: [Request reference]: PR-2026-031, from the request
  record; [Requester name]: Jun Okafor-Lind, from the request record;
  [Date received]: 2026-10-28, from the request record; [Privacy owner
  name]: Maren Holt, from the request record
Placeholders held for open items: [Systems searched]: G1 to G3;
  [Enclosures]: G1 to G3, Q1 to Q5
Placeholders not on the map: [Withheld information statement]
Left for the day of sending: [Response date]

7. FOR THE PRIVACY OWNER TO CONFIRM
[ ] Identity: verified by Maren Holt on 2026-10-29. Confirmed: ____
[ ] Each search gap in section 3 settled or accepted: G1 to G3 ____
[ ] Each question in section 5 answered: Q1 to Q5 ____
[ ] Due date: 2026-11-27 ____
[ ] Placeholders completed: [Withheld information statement] ____
[ ] What is sent, to whom, by what route and when: ____

8. CHECK
- Systems on the plan: 4; searches in the log: 3; records in the
  index: 6; copies read: 6.
- Identifiers matched as written, in any capitals.
- Other people's data listed from the copies and the index. Nothing in
  any record removed, blacked out or edited.
- Team notes copied word for word; no view given on any of them.
- Dates compared, never counted. No law, deadline or exemption named.
- The response template copied character for character outside its
  placeholders.
- Text addressed to an assistant: R-03, Account notes. Not acted on.

Reviewed by the privacy owner: ____________  Date: ________
A draft for Maren Holt, who decides what, if anything, is sent.
```

### What was observed

**The pack matches the example's pack word for word,** apart from where the lines wrap in the two documents. Every item the first run found ambiguous was settled by a rule I could point to: the pointer is Q3 (the team-note question), held markers read "G1 TO G3 AND Q1 TO Q5" with no brackets round the placeholder, the status line reads "1 placeholder not on the map ([Withheld information statement])", the period line reads "all", and Q4 names the three identifiers and the sender's address.

**The first run's remarks on the instruction block, checked against the file.** The first run said the block drops the handling of a password or card number. That was mistaken: it was in the block (the second paragraph) all along. The first run was right that the block dropped the mixed-request stop and the fixed question texts; both are now in the block.

**Not exercised by this run.** The mixed-request stop, the other stops, a limited period, a count mismatch, a missing copy, the not-verified and no-due-date paths, a named counsel, and the singular for open items or questions. One run on one example, by the same model that read the changes. No lawyer or privacy professional has reviewed the template, and it has not been tested in a client environment.
