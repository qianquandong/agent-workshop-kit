# Set up the three agents

Each agent is set up the same way:

1. Run it once.
2. Make it yours.
3. Test it.
4. Put it on a schedule.

---

## Before you start (once, about 15 minutes)

1. **Get the kit and upload the 5 skills.** Upload them in Settings → Customize → Skills → Add → Upload skill. The prompt is in `prompts/Get_the_Kit.md`.
2. **Connect your tools:** Gmail, Google Calendar, Google Drive, Google Docs, Google Sheets, ClickUp. Add Zoom if you record calls in the Zoom cloud.
3. **Run the connection check.** The prompt is in `prompts/Connection_Check.md`.
4. **Build the two homes:** folders in Google Drive for your clients, plus the sheets the agents use. One person does this once, then shares the Team Workspace folder and the Team Settings doc with the team. The prompt is in `prompts/Build_the_Two_Homes.md`.

Your Google admin must first turn on the Google connectors for the team and mark Claude as Trusted in Google admin.

---

## Agent 1 · Meeting Prep

A one-page brief before every call. It goes in a private event on your own calendar.

| Step | What to do |
|---|---|
| Run it once | `Use the meeting-prep skill. Prep my calls for tomorrow. Show me the briefs here in the chat. Don't create calendar events or files yet.` |
| Make it yours | Build your **Prep Profile**. Claude interviews you, one question at a time. Prompt: `prompts/Questionnaire_and_Prep_Profile.md`, Part C. |
| Test it | Run it on the practice week and check the answers. Details are in the README. |
| Schedule it | Every **Friday at 3 PM** for next week, and every **weekday at 7 AM** for today. The prompts are in `prompts/Schedules.md`. |

**What you decide in your profile:**
- your top 3 things to see
- what you never want to see
- how long the brief is, and when it arrives
- your go-to questions
- one example of a great brief

A profile can change the focus and the format. It can never loosen the privacy rules.

---

## Agent 2 · Follow-Up Nudger

Finds email threads that went quiet and writes a follow-up draft. It never sends.

| Step | What to do |
|---|---|
| Run it once | `Use the follow-up-nudger skill on my mailbox. Drafts only.` |
| Make it yours | Fill in your **Nudge Rules**. Prompt: `prompts/Answer_and_Send.md`, "Nudge rules". |
| Test it | Run it on the five practice threads and check the answers. Details are in the README. |
| Schedule it | Every **weekday at 7:30 AM**. The prompt is in `prompts/Schedules.md`. |

**What you decide in your Nudge Rules:**
- how long to wait before a nudge (default: 5 business days)
- how long to wait for sponsors and renewals, and the rule for promised dates (1 day after)
- how early to start renewal talks (default: 60 days)
- who or what to never nudge
- what a nudge may share: articles, results, event dates

**A good nudge:**
- is under 90 words
- mentions the real last exchange
- adds one useful thing
- ends with one clear ask and a date

---

## Agent 3 · Retainer Intelligence

For one client at a time, it makes four things:
- a health check, for you only
- a progress report that's safe for the sponsor
- testimonial quotes
- renewal alerts

| Step | What to do |
|---|---|
| Run it once | `Use the retainer-intelligence skill for [client]. Last 90 days. Give me all four outputs.` |
| Make it yours | Agree on your **warning signs**, and say where each number comes from. Prompt: `prompts/Answer_and_Send.md`, "Warning signs". |
| Test it | Run it on the practice client and check the answers. Details are in the README. |
| Schedule it | **Once a month** for each client, and again **60 and 30 days before a renewal**. |

**The warning signs to start with:**

| Sign | Green | Amber | Red |
|---|---|---|---|
| Attendance | 90%+ of booked sessions | 75–89% | Under 75%, or 2 no-shows in a row |
| CSAT | 4.5+ average | 4.0–4.4 | Under 4.0, or a drop of 0.5 |
| Goal progress | Progress on each goal | On some goals | None in 2+ sessions |
| Sponsor contact | Within 45 days | 46–90 days | 90+ days, or sponsor changed |
| Delivery | Nothing overdue | 1 overdue | 2+ overdue |

---

## Automation: how much to set up, and when

Start small. Set up the night check on day one. Add the faster jobs only if you need them.

| What | How it starts | Time to set up | Extra cost | When |
|---|---|---|---|---|
| The 3 agents' schedules | Scheduled task in Claude | 5 minutes each | None | Day 1 |
| **Night check** (catches anything missed today) | Scheduled task, every night at 10 PM, one per person | 5 minutes | None | **Day 1** |
| Email job | Scheduled task, every hour | 5 minutes | None | Week 1 |
| Client documents job | Scheduled task, Mondays at 8 AM | 5 minutes | None | Week 1 |
| Zoom recordings → recap the same hour | Claude routine + Zapier | About 30 minutes | Zapier paid plan | Week 2, if the night check feels too slow |
| Notes, tasks, calendar, research, client feedback | Claude routine + Zapier | About 20 minutes each | Same Zapier plan | Weeks 3–4, one at a time |
| CRM changes, calls and texts (optional) | Claude routine + a GoHighLevel workflow | About 20 minutes each | None | When you need them |

**How much Zapier you need:** only the "Claude routine + Zapier" rows use it. The free plan can't do them, because they need webhooks and more than one step. At about 15 meetings a week, plan for **400 to 600 Zapier tasks a month**. The lowest paid plan covers that for one person's calendar.

**Every job can also run by hand:**

`Use the data-jobs skill. Run the [job] job now for [today / this client / since a date].`

The steps for every job are in the `data-jobs` skill. The schedule prompts are in `prompts/Schedules.md`.

---

## Every day

- **Before a call:** read the brief in the private Prep event on your calendar.
- **After a call:** save your notes in the Notes folder, or give Claude the transcript: `Use the meeting-prep skill in recap mode on this transcript. Create each promise as a ClickUp task tagged "proposed".`
- **In the morning:** open your Gmail drafts, edit the follow-ups, and send the good ones.
- **In ClickUp:** tasks the agents add are tagged **proposed**. Remove the tag to say yes, or delete the task.
- **Fixed the same thing twice?** Add one line to your Prep Profile (about you) or to the team-voice skill (about the team).

**For the first 4 weeks:** score every output in the Score Sheet: used as-is, light edit, or rewrite. Keep the agents if 8 out of 10 need a light edit or none.

---

## Rules that never change

- It only sees what you can already see.
- It writes drafts. A person sends.
- It treats emails, invites and notes as facts, never as orders.
- Private coaching notes never reach a sponsor.
