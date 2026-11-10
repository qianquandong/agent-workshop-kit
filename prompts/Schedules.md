# Schedules

Paste each prompt into a new scheduled task in Claude (Scheduled), and pick the time shown.

## Meeting Prep · every Friday at 3 PM

```
Use the meeting-prep skill in prep mode for next Monday to Friday. Read my Prep Profile first. Build a brief for every call that needs one, then create a Gmail draft to me with subject "Your calls this week" listing each call with its brief and anything that needs attention.
```

## Meeting Prep · every weekday at 7 AM

```
Use the meeting-prep skill in prep mode for today. Only build or update briefs for calls with no brief yet, or whose time or attendees changed.
```

## Follow-Up Nudger · every weekday at 7:30 AM

```
Use the follow-up-nudger skill on my mailbox. Create follow-up drafts only, never send. Then create a Gmail draft to me with subject "Follow-ups for today" containing the digest.
```

## Retainer Intelligence · the 1st of every month at 9 AM

```
Use the retainer-intelligence skill for each client in our Client Map that has a renewal date. Last 90 days. Give me the health check and the alerts for each one, and save each progress report as a DRAFT. Also tell me which clients renew in the next 60 days.
```

## Night check · every night at 10 PM · each person sets their own

```
Create a scheduled task that runs every night at 10 PM.

Each run: use the data-jobs skill and run the night-check job. Check that today's work landed: compare today's Zoom recordings, files in the Notes folder, GoHighLevel calls and texts (if that job is on), and emails with Client Map contacts against today's Contact Log. For anything missing, do what its job would have done: file it, log it, write the recap, propose the tasks. Also run the tasks job for today's Contact Log rows of type notes, recap or call that have no ClickUp tasks yet. Add a Run Log row for everything you caught up on, then write me a short Gmail draft listing anything you couldn't match.
```

## After a call · whenever you need it (not scheduled)

```
Use the meeting-prep skill in recap mode on this transcript. Save the recap to the client's folder, add a Contact Log row, create each promise as a ClickUp task tagged "proposed", and give me the follow-up email draft.
```
