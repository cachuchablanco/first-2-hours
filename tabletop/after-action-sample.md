# After-action sample (dry run)

**Exercise:** Cedar Ridge Community Clinic — First 2 Hours  
**Date of dry run:** 2026-08-26  
**Facilitator / scribe:** Oscar Hernandez  
**Players:** IT Lead (IC), Director, Charge RN, Billing  
**Duration:** 88 minutes  
**Lab only. Not a real incident.**

## What we were testing

Can four people contain, keep care going, and tell the truth about backups in two hours with no SOC.

## Compressed log

| Time | Event | Decision |
|------|--------|----------|
| 07:40 | Two reception PCs + scheduling down | IT took IC. Photographed note. Did not click. Pulled Director. |
| 07:48 | Isolated reception and billing | Left one dirty PC. Did not reimage. |
| 08:00 | EHR spinner, shared drive dead | Disabled staff VPN. Phones stayed up. |
| 08:12 | Patient at desk | Stay open on paper for scheduled visits only. No new walk-ins. |
| 08:20 | Staff note via cell, not email | Comms = Director only. |
| 08:40 | NAS "success at 02:12" still mounted | Did **not** restore. Unmounted NAS from workstation VLAN. USB stayed in the bag. |
| 08:50 | Decryptor idea from a phone | Shut down. Logged as a near-miss. |
| 09:15 | Reporter + "email the patients?" | No comment. No patient email. Insurance callback. EHR vendor ticket. |
| 09:35 | Hand-off | IC through 18:00. Next checkpoint 10:40. Paper until a real backup plan exists. |

## What went well

- Someone said "I have it."
- Isolated instead of wiping.
- Clinical owned stay-open. IT did not promise a time they could not hit.
- USB stayed out of the sick PCs.
- Press and patient notice waited.

## What would have failed for real

- Restore had **never been tested**. "NAS job succeeded" was comfort for too long.
- Phone tree lived in the IT lead's head.
- Downtime forms were incomplete. Charge RN only caught it because a patient was standing there.
- No pre-written staff note. They spent nine minutes drafting.

## What I would actually change

1. Print this checklist and the phone tree. Put both in the downtime binder **and** in a personal phone. The shared drive dies in this scenario.
2. Test a restore this quarter. A successful backup job is not a restore.
3. Treat the NAS as in-scope until proven otherwise. Same network is not offline.
4. One comms owner, two sentences, pre-approved. Patient notice is a legal call, not a billing call.
5. Default: do not pay, do not decryptor-shop.

## If I had 20 seconds with a hiring manager

The first two hours are not "find the malware family." They are command, containment, backup truth, and not making care or evidence worse. This dry run failed the restore-test and the phone-tree. That is the point of doing it before a Monday at 07:40.
