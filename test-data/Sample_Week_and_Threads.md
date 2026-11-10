# FICTIONAL SAMPLE DATA FOR WORKSHOP TESTING

Use this when you don't want to run the agents on real client data yet. Paste it into Claude together with the request, e.g. "Use the meeting-prep skill on this sample week instead of my calendar."

## Sample calendar (Sam's calendar, week of Nov 16, 2026)

In every sample you are **Sam** (sam@brightpath-example.com). Your teammates are Alex and Morgan. The sample Team Settings file says so too.

| Day / time (CT) | Title | Attendees | Notes |
|---|---|---|---|
| Mon 9:00–9:15 | Team Standup (recurring) | sam@, alex@, morgan@brightpath-example.com | |
| Mon 11:00–12:00 | Northbeam – Quarterly sponsor check-in | rachel.ortiz@northbeam-example.com, sam@, alex@ | |
| Tue 10:00–11:00 | Coaching – Dana R. | dana.reyes@northbeam-example.com, sam@ | |
| Tue 12:00–13:00 | Lunch | (none) | personal |
| Wed 14:00–14:30 | Intro – Trinity Steel | cmendes@trinitysteel-example.com, sam@ | proposal sent 10/28 |
| Thu 15:00–15:30 | Chat | j.lowe@unknown-example.net, sam@ | no other info |
| Fri 9:00–9:30 | Morgan / Sam 1:1 | morgan@, sam@ | |

Expected behaviour to check:
- Standup and Lunch are skipped.
- Northbeam sponsor check-in: rule 2, no coaching content about Dana.
- Coaching – Dana R.: rule 1, coaching notes allowed, brief stored in the Private folder.
- Trinity Steel: sales template.
- "Chat" with an unknown address: NEEDS MATCH + UNSURE type, no guessing.

## Sample sent threads (Sam's Gmail) for the Follow-Up Nudger

**Thread A – Trinity Steel proposal** (today = Tue Nov 10)
- Oct 28, Sam → Carla Mendes: "Great meeting you at the Spring Summit. Attached is the Team Program proposal for your plant managers' cohort, starting February. Happy to walk your CFO through the numbers."
- No reply since. → 9 business days quiet, nudge 1 expected.

**Thread B – Lakeside renewal**
- Oct 20, Mark Ellison → Sam: "Let me check budget and come back to you by Nov 6."
- Oct 20, Sam → Mark: "Thanks Mark, talk then."
- Nothing since. → past his promised date, nudge 1 expected.

**Thread C – Cobalt Logistics (FICTIONAL)**
- Sep 30, Sam → Ben: first nudge (label Nudge-1).
- Oct 14, Sam → Ben: second nudge (label Nudge-2).
- No reply. → Decision needed, no draft.

**Thread D – Westfield Group (FICTIONAL), contact Tara Wells, tara@westfield-example.com**
- Oct 15, Sam → Tara: "Following up on the pilot scope we discussed."
- Nov 2, Alex emailed Tara from her own mailbox (there is a row for it in the Nudge Log template).
- → Skip: owned by Alex.

**Thread E – Harbor Credit Union (FICTIONAL)**
- Nov 3, contact → Sam: "We need to cancel the December workshop, our CEO is leaving. Can we talk about the deposit?"
- Nov 3, Sam → contact: "So sorry to hear that, let me check and come back to you."
- → Sensitive (cancellation + money): no draft, listed under Decision needed.
