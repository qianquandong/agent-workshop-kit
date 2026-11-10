---
name: retainer-intelligence
description: For one retainer client at a time, reads session recaps/transcripts, CSAT and engagement data and turns them into (1) a sponsor-safe progress report draft, (2) testimonial candidates that still need written consent, and (3) renewal, expansion and risk flags with evidence. Use for the monthly client review, 60/30 days before a renewal, or when asked "how is <client> doing?".
---

# Retainer Intelligence

Goal: every retainer client gets a regular, evidence-based picture of progress, and we see renewal and expansion chances (and risks) early instead of at renewal time.

You draft. Nothing goes to a client, sponsor or website without a person reviewing it.

## Step 0. Check the data is fresh

Look at the Run Log for the recordings, notes, experience and crm jobs. If one is too old (the data-jobs skill says what "too old" means), run it yourself with the data-jobs skill for this client only, then follow its catch-up steps: log it, find the likely reason, draft a note to the system owner (named in the Team Settings doc; if there is none, me). Say so at the top of the Client Review. If there is no Run Log or no data-jobs skill yet, skip this check and say so.

## Inputs (for the one client named)

| Source | Where | Notes |
|---|---|---|
| Client Map row | "Client Map" sheet | program, sponsor, coach, contract dates, renewal date |
| Session recaps | client folder, files starting "Recap –" | preferred over raw transcripts |
| Raw transcripts | client Private folder (Zoom transcripts) | only if no recap exists for that session |
| CSAT / feedback | "Client Experience" sheet | score per session or survey |
| Engagement | Client Experience sheet / ClickUp | sessions booked vs attended, no-shows, workbook completion |
| Delivery | ClickUp client list | milestones, overdue deliverables |
| Goals | proposal or goals doc in the client folder | what the client signed up to achieve |
| Sponsor contact | Contact Log sheet, recaps of sponsor check-ins | date of the last check-in |

Period: the last 30 days by default (or what the user asks for), plus the full contract to date for trends. The "prior period" is the same number of days just before it. State the period at the top of every output.

If a source is missing, write "not available" for it. Never estimate a number.

## Output 1. Client health snapshot (internal only)

| Signal | Green | Amber | Red |
|---|---|---|---|
| Attendance | ≥ 90% of sessions held | 75–89% | < 75% or 2 no-shows in a row |
| CSAT | average 4.5 or more | 4.0 to 4.49 | under 4.0, or the average fell by 0.5 or more vs the prior period |
| Progress on goals | recaps show progress on each goal | progress on some | no progress mentioned in 2+ sessions |
| Sponsor engagement | check-in in the last 45 days | 46–90 days | none in 90 days or sponsor changed |
| Delivery | no overdue deliverables | 1 overdue | 2+ overdue |

Counting attendance: count each session number once. A session that was moved and then held within 14 days counts as held; note it as a reschedule. A no-show is a booked session that was never held.

Overall: if any signal is red, overall is red. Otherwise, if any is amber, overall is amber. Otherwise green. A signal with no data is "not available": leave it out of the color, and say how many are missing (for example "Green so far, 3 of 5 not available"). Give one line of evidence for every non-green signal, with a link when the Client Map has one (a cell that still says "<paste link>" counts as no link).

## Output 2. Sponsor-safe progress report (draft)

For the sponsor / HR contact. Strict rules:
- Content allowed: program goals as agreed in the proposal, sessions held, attendance, CSAT averages, milestones delivered, themes the coachee said are OK to share with the sponsor (the "OK to share with sponsor" section of a recap, or the coachee's own clear words in a transcript).
- Not allowed: quotes from sessions, personal details, anything from the Private folder that is not explicitly approved, any judgment of the coachee's performance.
- Shape: 1 page. Program at a glance (numbers) → progress against each goal (2–3 lines each, approved themes only) → what's next (next 30–60 days) → one question for the sponsor.

Add at the top: "DRAFT – coach to review; coachee to approve any themes before sending."

## Output 3. Testimonial candidates

From recaps and transcripts, pull up to 3 statements where the client describes a result or a change in their own words.
For each: exact quote, date, source link, what result it shows, and a suggested short version (no new words added).
Mark every candidate: "Needs written permission before any use." Never put a candidate on a website, proposal or post. Quotes from coaching sessions are private: they go only in the Private copy (see Finish).

## Output 4. Renewal, expansion and risk flags

List each flag with: type, evidence, suggested action, owner (the coach_owner in the Client Map), and by when (renewal: at least 30 days before the renewal date; everything else: within 7 days).
- **Renewal**: renewal date within 60 days → prepare renewal conversation; include the 3 strongest outcomes to mention, using only numbers and approved themes.
- **Expansion**: someone new who wants coaching, a new cohort, a team that wants the same, a promotion, budget timing.
- **Risk**: any red signal, sponsor change, a restructure, budget freeze, CSAT average down by 0.5 or more, a no-show.

If the coachee asked to keep a person or a topic private, never raise it as a flag and never put it in Output 2. Keep the list short: only flags a person should act on.

## Finish

Return the four outputs in this order. Save outputs 1 and 4 as one internal doc `Client Review – YYYY-MM – <Client>` in the client's internal folder (YYYY-MM is the month you run it). Save output 3 as `Testimonial quotes – YYYY-MM – <Client>` in the client's Private folder. Save output 2 as a separate doc `Progress Report DRAFT – YYYY-MM – <Client>` in the internal folder.

Check before finishing: every number has a source; nothing private is in output 2; every testimonial says it needs permission.
