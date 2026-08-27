# Facilitator guide (90 minutes)

**Audience:** small-org staff, not a SOC. Also works as a portfolio walkthrough in an interview: "here is how I would run the first two hours."

**Materials:** printed [checklist](../checklists/first-2-hours.md), [roles](roles.md), [injects](injects.md), a timer, a whiteboard for the incident log.

## Setup (5 min)

- Assign seats. If a real clinic is playing, use their titles.
- State the ground rules: no malware, no real PHI, no "I would hack them back."
- Write the clinic's **actual** backup sentence on the board before inject 1, or use the lab sentence: "Nightly NAS. Weekly USB someone takes home. Restore last tested: unknown."

## Run of show

| Clock | Block |
|-------|--------|
| 0:00–0:05 | Setup |
| 0:05–0:20 | Inject 1 — discovery. Let them fumble comms. |
| 0:20–0:40 | Inject 2 — spread / more PCs. Force a contain decision. |
| 0:40–0:55 | Inject 3 — clinical impact (cannot schedule, one patient at the desk). |
| 0:55–1:10 | Inject 4 — backup truth and a bad idea (USB, decryptor, pay). |
| 1:10–1:20 | Inject 5 — reporter / "are we notifying?" |
| 1:20–1:35 | Decisions for the next 24 hours |
| 1:35–1:50 | Hotwash: what was missing before today |

## What you are scoring (not "did they guess the malware")

1. Did someone take IC, or did three people give orders?
2. Did they isolate without wiping?
3. Did clinical get a vote on stay-open vs divert?
4. Did they treat backups as a question, not an assumption?
5. Did they keep comms on a clean channel?
6. Did they write decisions down?

## Interview version (15 min)

If this is for a hiring manager, skip the role-play. Walk the checklist out loud with the sample AAR in hand. That is the demo.
