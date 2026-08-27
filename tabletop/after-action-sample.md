# After-action sample (dry run)

**Exercise:** Cedar Ridge Community Clinic — First 2 Hours  
**Date of dry run:** 2026-08-26  
**Facilitator / scribe:** cachuchablanco  
**Players:** IT Lead (IC), Director, Charge RN, Billing  
**Duration:** 88 minutes  
**This is a lab writeup, not a real incident.**

## What we were testing

Can a four-person clinic make containment, care, and backup decisions in two hours without a SOC and without making it worse.

## What happened (compressed log)

| Time | Event | Decision |
|------|--------|----------|
| 07:40 | Two reception PCs + scheduling down | IT took IC. Photographed note. Did not click. Director pulled from meeting. |
| 07:48 | Isolated reception switch ports and billing PC (unplug) | Left one dirty PC bagged. Did not reimage. |
| 08:00 | EHR loading spinner, shared drive dead | Disabled staff VPN. Phones kept up. |
| 08:12 | Patient at desk | Director + Charge RN: stay open on paper for scheduled in-clinic only. No new walk-ins. |
| 08:20 | Internal note via cell group, not email | Comms = Director only. |
| 08:40 | NAS "success at 02:12" still mounted | Did **not** restore yet. Unmounted NAS from workstation VLAN. USB stayed in the bag. |
| 08:50 | Decryptor idea from a staff phone | Shut down. Logged as a near-miss. |
| 09:15 | Reporter + "email the patients?" | No comment. No patient email. Insurance called, callback set. EHR vendor ticket opened. |
| 09:35 | Hand-off | IC through 18:00 = IT Lead. Next checkpoint 10:40. Clinic remains paper until vendor + backup plan exists. |

## What went well

- Someone actually said "I have it."
- They isolated instead of wiping.
- Clinical owned stay-open. IT did not promise a time they could not hit.
- USB was not plugged into a dirty PC.
- Press and patient notification waited.

## What would have failed in real life

- Restore had **never been tested**. "NAS job succeeded" was treated as comfort for too long (about 15 minutes of discussion).
- Comms list lived in the IT Lead's head. If they were out, Director did not have insurance or vendor numbers.
- Downtime forms were incomplete. Charge RN caught it only because Inject 3 forced a patient at the desk.
- No pre-written "systems down" staff note. They spent nine minutes drafting.

## Recommendations (the actual portfolio output)

1. **Print this checklist and the phone tree.** Put both in the downtime binder and in a personal phone, not only on the shared drive that dies in this scenario.
2. **Test a restore this quarter.** A successful backup job is not a restore. Pick one EHR-adjacent share and restore it to a dark VM or a vendor-supported process. Write the date on the checklist.
3. **Treat the NAS as in-scope until proven otherwise.** Nightly backups sitting on the same network are not offline.
4. **One comms owner, two sentences, pre-approved.** Staff note and "no comment" for press. Patient notice is a legal call, not a billing call.
5. **Default: do not pay, do not decryptor-shop.** Leadership + insurance if that ever becomes a real question.

## What I would tell a hiring manager

The first two hours are not "find the malware family." They are command, containment, backup truth, and not making care or evidence worse. This dry run failed the restore-test and the phone-tree, which is the point of tabletopting before a Monday at 07:40.
