# Injects

Read these to the room. Do not hand out the whole pack in advance.

All technical detail is at the level a clinic would actually see. There is no malware sample and no payload.

## Inject 1 — 07:40 · Discovery

Front desk: "Scheduling won't open. Two other PCs in reception have a full-screen note I don't want to read out loud. Phones still work."

IT is on site. Director is in a meeting. First patients are at the door.

**Watch for:** who gets called first, whether someone starts rebooting PCs, whether the note gets photographed or clicked.

## Inject 2 — 07:55 · It is not one PC

Charge nurse: "Nurses' station is slow. Shared drive with downtime forms is spinning. The EHR window is stuck on loading. The PC in billing has the same note as reception."

**Watch for:** network isolation vs pulling the building internet, whether they disable VPN/remote access, whether they keep one dirty box instead of wiping all of them.

## Inject 3 — 08:15 · Care is the incident too

Director is now in the room. A patient is at the desk for a lab draw. Paper downtime forms are in a binder in billing, last restocked last year. Nobody is sure the medication list printouts are current.

**Watch for:** Director vs IT on stay-open, Charge RN actually owning paper flow, someone saying "IT will have it up in 20 minutes" with no basis.

## Inject 4 — 08:35 · Backup and a bad idea

IT, if they look: last NAS backup job shows **success at 02:12**. The NAS is still on the same network as the workstations. The weekly USB is in the IT lead's backpack, last used "a few weeks ago," and they are about to plug it in "to see if the files are there." A well-meaning staffer has searched for a decryptor on their phone.

**Watch for:** do they stop the USB, do they assume NAS is clean, do they call the EHR vendor, do they treat "successful job" as "restored and known-good."

## Inject 5 — 09:10 · Outside world

A local reporter DMs the clinic Facebook page: "Hearing you're closed because of a cyber attack. Comment?" Billing asks if they should email yesterday's patients. Insurance voicemail: "If this is a claim, do not hire a random firm before you call us."

**Watch for:** one comms owner, no patient notification in hour two without counsel, no comment to press, insurance before a cold-call IR firm.

## Optional hard mode (only if the room is cruising)

EHR vendor is on-prem and the application server shows the same note. Restore from NAS would take "maybe tonight" and has never been tested. USB copy is from 19 days ago.
