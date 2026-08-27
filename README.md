# First 2 Hours

A ransomware tabletop for a small organization that does not have a SOC. Roles, comms, backups, and what you actually do before leadership panics.

No malware. No exploit steps. No encryptor. The incident is a prompt. The portfolio is the process.

**Author:** [cachuchablanco](https://github.com/cachuchablanco) · junior cybersecurity · IR / SOC / analyst roles

**Lab org:** Cedar Ridge Community Clinic (fictional nonprofit clinic, ~80 staff, one IT person)

## Why this exists

Small clinics, schools, and nonprofits get hit and then freeze. Junior IR jobs still ask "what would you do in the first two hours?" This repo is a written answer you can run as a 90-minute tabletop, plus a sample after-action from a dry run.

Pairs with [capsule-corp-phish-desk](https://github.com/cachuchablanco/capsule-corp-phish-desk) (email triage). That one is a ticket queue. This one is a room full of people.

## Skills this shows

- Incident command for a shop with no 24/7 SOC
- Who talks to whom (IT, clinical leadership, legal, insurance, patients)
- Evidence-preserving containment vs "just pull the plug"
- Backup reality checks (last known good, offline copy, restore test)
- Decision logging a later investigator can use
- After-action writing

## What's in here

| File | What a hiring manager gets |
|------|----------------------------|
| [checklists/first-2-hours.md](checklists/first-2-hours.md) | Minute-by-minute job aid for the first 120 minutes |
| [tabletop/roles.md](tabletop/roles.md) | Who is in the room and what they own |
| [tabletop/facilitator-guide.md](tabletop/facilitator-guide.md) | How to run it in 90 minutes |
| [tabletop/injects.md](tabletop/injects.md) | Timed prompts (discovery → patient impact → reporter) |
| [tabletop/after-action-sample.md](tabletop/after-action-sample.md) | Completed AAR from a dry run of this scenario |

## How to read this (about two minutes)

1. This README.
2. The [first-2-hours checklist](checklists/first-2-hours.md). That is the actual job.
3. Skim the [sample after-action](tabletop/after-action-sample.md) if you want to see judgment, not just a template.

## Scenario in one paragraph

Monday 07:40. Front desk cannot open the scheduling system. A few workstations show a ransom note on the lock screen. EHR is slow, then unreachable. The one IT staffer is on site. There is a nightly backup to a NAS, and a weekly USB copy that "someone takes home." Nobody has restored it this year. No dedicated security team.

## What this is not

- Not a ransomware builder, decryptor, or malware analysis lab
- Not a playbook for attacking anyone
- Not legal, clinical, or insurance advice
- Clinic, staff, and reporter names are fictional

If you run this at a real org, swap in their names and their backup truth. The clock stays the same.
