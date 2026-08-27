# First 2 hours — job aid

Print this. Do not start from a blank page at 07:40. Kakarot energy is for later. Right now you need a clock and one voice.

**Incident name:** Cedar Ridge Clinic — suspected ransomware  
**Clock starts:** when it is not "one PC"  
**Incident commander (IC):** ____________  backup: ____________

This is containment and decisions. It is not malware reverse engineering.

## 0:00–0:10 · Stabilize the room

- [ ] IC says out loud: "I have it." One voice. Others execute. Vegeta can be IC. Two Vegetas cannot.
- [ ] Start one incident log (time, who, what, decision). Phone notes beat five group chats.
- [ ] Split **clinical safety** from **IT**. Patients still need a path of care.
- [ ] If a ransom note is on a screen, photograph it. Do not type in it. Do not click it. Do not reboot "to see."

## 0:10–0:25 · Stop the bleeding

Goal: stop spread without destroying evidence.

- [ ] Isolate obviously affected PCs (unplug / kill Wi-Fi). Do not reimage yet.
- [ ] Disable shared drives / VPN / remote access if that is how sites talk.
- [ ] Leave one dirty machine as-is if anyone can image later. If nobody can, still do not wipe in hour one.
- [ ] Write what is **still up**: phones, internet, EHR, email, badges, backups.
- [ ] One-line status: what is down, what is up, can care continue on paper.

Do not:

- Pay, negotiate, or "just ask what they want"
- Download a random decryptor
- Blast "we got hacked" from a mailbox that might be dirty

## 0:25–0:40 · People

- [ ] Call the pre-agreed list only. See [roles](../tabletop/roles.md).
- [ ] Use a channel you still trust (cell phones). Not clinic email if it is acting weird.
- [ ] Clinical lead decides: stay open on paper, divert, or close. IT does not make that call alone.
- [ ] One person owns outside comms. Nobody else posts or emails patients.

Draft, do not send yet:

```
Scheduling and some workstations are down. We are containing a suspected incident.
Use paper fallback. Do not try to fix a PC that shows a note. Call [IC] with anything new.
```

## 0:40–1:10 · Backup truth

Ask out loud. Write the answers. Guessing is how you restore the infected copy.

- [ ] Last **successful** backup of EHR / scheduling / shares: date, time, where it lives
- [ ] Is there an **offline** copy that was not mounted this morning?
- [ ] Did anyone plug the USB "home copy" into a sick PC today? If yes, treat it as sick.
- [ ] Last restore **test**: date, or "never"
- [ ] EHR: cloud or on-prem. Cloud → call the vendor. On-prem → stop power-cycling the server
- [ ] Save: note photo, hostnames, last-good backup ID, any logs you can export without installing new toys in a panic

## 1:10–1:40 · Next 24 hours

IC + Director, in one sitting:

1. **Care:** open / divert / close today
2. **Restore vs rebuild:** do we have last-known-good, or paper until a vendor lands?
3. **Help:** insurance, IR firm, EHR vendor, MSP. Call the one with a contract. Hour two is late to shop.
4. **Legal / privacy:** if patient data may be involved, legal gets facts, not a theory. Do not notify patients in hour two unless counsel says so. Wrong notice is its own incident.
5. **Ransom:** default is do not pay. That is leadership + legal + insurance, not IT in a hallway.

If it is not written, it did not happen.

## 1:40–2:00 · Hand-off

- [ ] 10-line status for the next person
- [ ] Who stays, who goes, who is on call at 18:00
- [ ] Next checkpoint (example 10:40). Do not dissolve into "we'll see"

## Out of scope for hour two (on purpose)

Malware family, decryptor shopping, full forensics, patient letters, press. Those eat the clock. They belong after containment and after someone who does this for a living is on the phone.
