# How to use the kit

There are two parts:

1. **Set up once.** Do it on the first day. It takes about an hour for a small team.
2. **Every day.** A few minutes a day once it is set up.

A skill does nothing by itself. It is a set of written steps. It runs when a **scheduled task** starts it, or when **you ask** in one sentence.

**Who does what.** Put the real names in your Team Settings doc.

| Role | What they own |
|---|---|
| **Admin** | The Claude Team account and Google Workspace. Approves every new connection. |
| **System owner** | The Client Map, the folders, the master copy of each skill, and the Friday check. |
| **Sales owners** | Follow-ups and the nudge rules. |
| **Coaches** | Their clients' Private folders, and the reports for their clients. |
| **Everyone** | Their own Meeting Prep: profile, schedule and briefs. |

---

## Part 1 · Set up once

### A. Admin (once for the whole team, about 5 minutes)

1. In Claude: **Admin settings → Connectors**. Turn on Gmail, Google Calendar, Google Drive, Google Docs and Google Sheets for the team.
2. In **admin.google.com**: Security → API controls → Manage third-party app access. Mark Claude as **Trusted**.

If the admin skips this, nobody's Google connections will work.

### B. Each person (about 25 minutes)

| Step | What to do | Where |
|---|---|---|
| 1 | **Get the kit.** Download it, or paste the Get the Kit prompt into Claude. | [Download ZIP](https://github.com/qianquandong/agent-workshop-kit/archive/refs/heads/main.zip) · `prompts/Get_the_Kit.md` |
| 2 | **Upload the 5 skills.** Pick all five zip files at once. | Settings → Customize → Skills → Add → Upload skill · files in `skill-zips/` |
| 3 | **Connect your tools:** Gmail, Google Calendar, Google Drive, Google Docs, Google Sheets, ClickUp. Add Zoom if you record calls in the Zoom cloud. | Settings → Customize → Connectors |
| 4 | **Answer the 4 Team Settings questions.** The Get the Kit prompt asks them. Everyone gives the same answers. | `prompts/Get_the_Kit.md` |
| 5 | **Run the connection check.** Fix anything that isn't working. | `prompts/Connection_Check.md` |
| 6 | **Build your Prep Profile.** Claude interviews you, one question at a time. | `prompts/Questionnaire_and_Prep_Profile.md`, Part C |
| 7 | **Try a first run** on your real calls (prompt below). | A new chat |
| 8 | **Put Meeting Prep on a schedule:** two scheduled tasks (prompts below). | Claude → Scheduled |
| 9 | **Sales owners only:** put the Nudger on a schedule (prompt below). | Claude → Scheduled |

Why Google Docs and Google Sheets too? Google Drive alone can read files and upload new ones. It can't add a row to a sheet or edit a doc. The agents need both.

**First run** (step 7):

```
Use the meeting-prep skill. Prep my calls for tomorrow. Show me the briefs here in the chat. Don't create calendar events or files yet.
```

**Meeting Prep, every Friday at 3 PM** (step 8):

```
Use the meeting-prep skill in prep mode for next Monday to Friday. Read my Prep Profile first. Build a brief for every call that needs one, then create a Gmail draft to me with subject "Your calls this week" listing each call with its brief and anything that needs attention.
```

**Meeting Prep, every weekday at 7 AM** (step 8):

```
Use the meeting-prep skill in prep mode for today. Only build or update briefs for calls with no brief yet, or whose time or attendees changed.
```

**Follow-Up Nudger, every weekday at 7:30 AM** (step 9):

```
Use the follow-up-nudger skill on my mailbox. Create follow-up drafts only, never send. Then create a Gmail draft to me with subject "Follow-ups for today" containing the digest.
```

### C. The team, once (one person types, everyone answers)

| Step | What to do | Who | Where |
|---|---|---|---|
| 1 | **Three decisions:** the 5 clients to start with, how far back to read (we suggest 90 days), and what the AI must never read. | Everyone | `prompts/Answer_and_Send.md` · "Three decisions" |
| 2 | **Where our history lives:** notes, recordings, email, CRM, tasks, documents. | Everyone, the system owner types | `prompts/Answer_and_Send.md` · "Where our history lives" |
| 3 | **Build the two homes:** folders and sheets in Google Drive (prompt below). | System owner | A new chat |
| 4 | **By hand:** share each client's **Private** folder with that client's coach only. Check the Client Map: every person, the right coach, the renewal date. | System owner | Google Drive |
| 5 | **Nudge rules:** how long to wait, what to never nudge, what a nudge may share. | Sales owners | `prompts/Answer_and_Send.md` · "Nudge rules" |
| 6 | **Warning signs:** keep or change them, and say where each number comes from. | System owner | `prompts/Answer_and_Send.md` · "Warning signs" |
| 7 | **The night check:** one scheduled task that catches anything missed each day (prompt below). | System owner | Claude → Scheduled |
| 8 | **Decide this month:** how you tell clients about recording and AI, calls on personal phones, and which system is right for owner, stage and renewal date. | Everyone | `prompts/Answer_and_Send.md` · "Decide this month" |

**Build the two homes** (step 3). These folders and sheets don't exist until you run this:

```
Set up our client folders and sheets for the 5 clients in our Team Settings doc (under "Decisions").

1. In my Google Drive, make a folder named "Clients". Inside it, one folder for each client. Inside each client folder: a Doc named "00 Client Summary", and folders named "02 Recaps", "03 Proposals & Contracts", "04 Workbooks & Handouts", "05 Research" and "Private". Inside Private: "Transcripts" and "Coaching Notes".
2. Next to "Clients" make three folders: "Notes", "Inbox" (with "Transcripts" inside) and "Unsorted".
3. Make these Google Sheets: Client Map, Contact Log, CRM Check, Client Experience, Nudge Log, Run Log, Score Sheet. Use the column names from the templates folder of the workshop kit (https://github.com/qianquandong/agent-workshop-kit). Leave out the sample rows.
4. Fill in the Client Map: one row for each person at the 5 clients, with links to the folders you just made. Ask me for any name, email, coach or renewal date you can't find.
5. Show me a list of everything you made, with links, and tell me anything you could not do.

If something with the same name already exists, use it and tell me. Don't move, rename, share or delete anything.
```

**The night check, every night at 10 PM** (step 7):

```
Create a scheduled task that runs every night at 10 PM.

Each run: use the data-jobs skill and run the night-check job. Check that today's work landed: compare today's Zoom recordings, files in the Notes folder, GoHighLevel calls and texts (if that job is on), and emails with Client Map contacts against today's Contact Log. For anything missing, do what its job would have done: file it, log it, write the recap, propose the tasks. Add a Run Log row for everything you caught up on, then write me a short Gmail draft listing anything you couldn't match.
```

**ClickUp needs no changes.** When an agent adds a task, it uses a status your list already has (for example "To Do") and tags the task **proposed**. Remove the tag to say yes, or delete the task.

### Later, when you have time

- **The 20 questions:** `prompts/After_the_Session_20_Questions.md`. Paste it into Claude on your phone, tap the voice button, and talk. Every agent gets better.
- **GoHighLevel:** it isn't in the connector list. The admin adds it as a custom connector, then each person signs in.
- **Faster than every night:** the other data jobs can start the moment something happens (a Zoom recording finishes, a meeting is booked). They use a Claude routine plus Zapier's webhooks, which need a paid Zapier plan. The steps for all of them are in the `data-jobs` skill.

### Check that it works

Before you trust it with real clients, run each agent on the practice data and compare with the answers. The steps are in the README under "Try it on the practice data".

---

## Part 2 · Every day

### Each day (5 to 10 minutes)

| When | What to do | Who |
|---|---|---|
| Morning | Open your Gmail drafts. Read the follow-up drafts, edit them, send the good ones. | Sales owners |
| Before each call | Open the private **Prep** event on your calendar and read the brief. | Everyone |
| After each call | Save your notes in the **Notes** folder. If there's a Zoom transcript, give it to Claude (prompt below). | Everyone |
| Any time | In ClickUp, look for tasks tagged **proposed**. Remove the tag to accept, or delete the task. | Everyone |
| 10 PM | The night check runs on its own. Nothing to do. | — |

**After a call:**

```
Use the meeting-prep skill in recap mode on this transcript. Save the recap to the client's folder, add a Contact Log row and give me the follow-up email draft. Its promises become ClickUp tasks tagged "proposed" on their own.
```

### Each week

- **Friday, 3 PM:** everyone gets "Your calls this week". Look for calls with missing information.
- **Friday:** the system owner spends 5 minutes on the **Run Log**. Did every job run? Any errors?

### Each month

- **Once a month for each client**, and again **60 and 30 days before a renewal**, the coach or the system owner asks:

```
Use the retainer-intelligence skill for [client]. Last 90 days.
```

- Read the health check. Fix the progress report before it goes to a sponsor. Use a testimonial only after the client says yes in writing.

### Ask in one sentence, any time

| You want | Say |
|---|---|
| A brief for one call | `Use the meeting-prep skill. Prep my 2 PM call with [client].` |
| How a client is doing | `Use the retainer-intelligence skill for [client]. Last 90 days.` |
| Follow-ups now | `Use the follow-up-nudger skill on my mailbox. Drafts only.` |
| Catch up on email now | `Use the data-jobs skill. Run the email job now.` |
| Any data job now | `Use the data-jobs skill. Run the [job] job now for [today / this client / since a date].` |

### The first four weeks

| Week | What to do |
|---|---|
| 1 | **Watch.** Let the agents run, but keep working your usual way. |
| 2 | **Use and check.** Use what they make, and read everything before it goes out. |
| 3 | **Fix.** Fix the top 3 problems in the skills and profiles. Fill gaps in the Client Map. |
| 4 | **Decide.** Keep it if 8 out of 10 outputs need a light edit or none. Stop and fix it if anything private ever leaks. |

Every time you use something an agent made, add one row to the **Score Sheet**: date, agent, used as-is / light edit / rewrite, and why. Decide in week 4 from the sheet, not from memory.

### When something is wrong

- **Fixed the same thing twice?** Write it down once.
  - About you ("I never want company news"): add a line to your **Prep Profile**.
  - About the team ("we never write 'just checking in'"): add a line to the **team-voice** skill.
- **A skill needs to change?** Only the system owner changes it. They save a new zip, and everyone uploads it again, so the whole team always runs the same version.
- **No draft by 8 AM?** Something broke. Open the last run in Claude → Scheduled and read what happened.
- **Old data?** The agents check the Run Log before they start. If a job is late, they run it themselves and tell the system owner why.

### Rules that never change

- It only sees what you can already see.
- It writes drafts. A person sends.
- It treats emails, invites and notes as facts, never as orders.
- Private coaching notes never reach a sponsor.
