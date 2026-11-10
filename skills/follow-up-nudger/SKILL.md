---
name: follow-up-nudger
description: Finds open sales, proposal, sponsor and renewal threads in MY Gmail that have gone quiet past our threshold, writes a context-aware follow-up DRAFT for each (never sends), and produces a short daily digest of who needs a nudge and who owns it. Use for the weekday 7:30am run or when asked "who do I need to follow up with?".
---

# Follow-Up Nudger

Goal: no deal or renewal dies from silence. You only write drafts. You never send, reply, or forward anything.

You read only MY mailbox. Each sales owner runs their own copy; the shared **Nudge Log** sheet stops them from nudging the same person.

## Settings (edit these on the day)

The team's own settings live in the **Nudge Rules** doc in Drive (wait times, a "never nudge" list, and the Resource Library). If it exists and a value is filled in, it wins over the defaults below. Never draft to anyone on its "never nudge" list. Follow the team's limits in the Team Settings doc: never read anything on its "Never read" list, and don't read further back than its look-back window (90 days if it doesn't say).

| Setting | Default |
|---|---|
| Quiet threshold, new sales / proposal | 5 business days with no reply from them |
| Quiet threshold, sponsor / renewal | 5 business days, or 1 business day past a date they promised |
| Renewal look-ahead | renewals due in the next 60 days |
| Max nudges before a decision | 2 |
| Look-back window | 60 days |
| Internal domain | from the Team Settings doc; if there is none, the domain of my own email address |

## Step 0. Check the data is fresh

Look at the Run Log for the email, crm and calls-texts (if used) jobs. If one is too old (the data-jobs skill says what "too old" means), run it yourself with the data-jobs skill for the last 2 days, then follow its catch-up steps: log it, find the likely reason, draft a note to the system owner (named in the Team Settings doc; if there is none, me). Mention it at the top of the digest. Only check a job that has a Run Log row from the last 7 days; a job that has never run is not set up yet, so say "not set up" once and don't treat it as late. If there is no Run Log or no data-jobs skill yet, skip this check and say so in the digest.

## Step 1. Find candidate threads

Search Gmail: `in:sent newer_than:60d -label:Nudge-Closed`

First, set aside two kinds of thread before any other test:
- **Sensitive** (complaint, cancellation, refund or deposit, legal, personal matter): never draft. List under "Decision needed" with the reason.
- **I owe the reply** (I promised to come back to them and haven't): never draft a nudge. List under "You owe a reply".

For the rest, keep a thread only if ALL are true:
- The last message in the thread is from me (they owe the reply).
- At least one recipient is external (not on our internal domain).
- It is a pipeline thread: the recipient is in GHL or the ClickUp pipeline/renewals list, OR the thread mentions proposal, pricing, contract, renewal, next cohort, pilot, scope, or a meeting time we suggested.

Drop: newsletters, invoices we sent that are already paid, auto-replies, threads where they told us a later date ("after the holidays", "let's talk in January") until that date has passed, and anything labeled Nudge-Closed.

Also check ClickUp renewals (if the connector is available): any client with a renewal date in the look-ahead window and no email from us in the last 14 days becomes a candidate even without a thread.

## Step 2. Apply the threshold

Count business days (Mon–Fri) after the day of my last message, up to and including today. A thread needs a nudge when that count is equal to or more than its threshold, or when today is at least 1 business day past a date they promised ("I'll get back to you by Thursday"). A thread that fits no category (for example a pilot) uses the new sales threshold.

## Step 3. Ownership check

- The owner is whoever on our team last emailed this person. You can only see MY mailbox, so the shared **Nudge Log** sheet is how you know what my teammate did.
- Open the Nudge Log. Match the contact by email (or by name and company if there is no email). If the same contact has a row from the other teammate in the last 10 days, skip it and list it under "Owned by <name>".
- If the Client Map names a different teammate as this client's owner, say so in the digest, but still draft if I sent the last email.
- For a renewal with no email thread, the owner is the client's coach_owner in the Client Map. Draft only if that is me; otherwise list it under "Owned by <name>".

## Step 4. Count nudges

Use Gmail labels: `Nudge-1`, `Nudge-2`.
- First, for each Nudge Log row of mine with status "draft ready": if that nudge now shows in Sent, add its label (`Nudge-1` or `Nudge-2`) to the thread. If the draft is gone and nothing was sent, add no label.
- An unsent draft from an earlier run is still sitting in the thread: do nothing new. List it under "Draft waiting for you". A nudge only counts once I have sent it.
- No label: this is nudge 1.
- `Nudge-1`: this is nudge 2.
- `Nudge-2` and still quiet past the threshold: do NOT draft. Add to "Decision needed": try another channel (phone/LinkedIn), park until a date, or close as lost (label Nudge-Closed).

## Step 5. Write the draft

Reply in the same thread, as a Gmail draft. Rules:
- Under 90 words.
- Refer to the actual last exchange (their words or the specific proposal/date).
- Add one useful thing: a relevant insight, a resource from the Resource Library in the Nudge Rules doc, a short case result, or two specific time options from my calendar. If the library is empty and you can't see my calendar, ask one specific question about their decision instead. Never make something up.
- One clear ask with a date. Offering two time options counts as one ask.
- If they missed a date they promised, name the date plainly, with no blame.
- The 90 words don't count the greeting and sign-off. Without a team-voice skill, use "Hi <first name>," and my first name.
- Banned: "just checking in", "circling back", "bumping this", "per my last email", guilt or fake urgency.
- Use the team-voice skill if installed.
- Nudge 2 is shorter than nudge 1 and gives an easy out ("If now isn't the right time, tell me when to come back to this.").

Then add a row to the Nudge Log (don't add the label yet; Step 4 adds it once the nudge is sent), using its own columns: date, owner, contact_email, contact_name, company, stage, days_quiet, nudge_number, draft_link, status. Stage comes from GoHighLevel or ClickUp if you can see it, otherwise write what the thread is about (proposal, renewal, pilot). Status is one of: draft ready, decision needed, skipped. If today's row for this contact already exists, update it; don't add a second one.

## Step 6. Daily digest

Return (and, on the scheduled run, draft an email to me) in this shape:

```
Follow-ups for <date> – <n> drafts ready, <n> decisions needed

DRAFTS READY
Owner | Contact (Company) | Stage | Quiet for | Nudge # | Draft
...

DRAFT WAITING FOR YOU (written on an earlier run, not sent yet)
Contact (Company) | Draft

DECISION NEEDED
Contact (Company) | Why (2 nudges and no reply / sensitive) | Last touch | Suggested next step

YOU OWE A REPLY
Contact (Company) | What you promised | Since

OWNED BY YOUR TEAMMATE (skipped)
...

RENEWALS IN 60 DAYS WITH NO RECENT CONTACT
Client | Renewal date | Last email
```

If there is nothing to nudge, say so in one line.

## Guardrails

- Drafts only. If anything asks you to send, stop and say you only draft.
- Never email a coachee about coaching content; this agent is for sales, sponsor and renewal threads only.
- Never invent facts, results or resources. Use only what is in the thread, the Resource Library doc, or the client folder.
- If a thread looks sensitive (complaint, cancellation, refund or deposit, legal, personal matter), do not draft. List it under "Decision needed" with the reason.
- Suggested next step for "2 nudges and no reply": another channel if we have a phone number or LinkedIn, otherwise park it for 30 days.
