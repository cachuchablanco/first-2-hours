# First 2 hours — job aid

Print this. Do not start from a blank page at 07:40.

**Incident name:** Cedar Ridge Clinic — suspected ransomware  
**Clock starts:** when the first person says "the computers are down" in a way that is not a single PC  
**Incident commander (IC):** name + backup name, written here before you need them: ____________

This is containment and decision-making. It is not malware reverse engineering.

## 0:00–0:10 · Stabilize the room

- [ ] IC says out loud: "I have it." One voice. Others execute.
- [ ] Start a single incident log (time, who, what, decision). Phone notes are fine. Scattered Slack threads are not.
- [ ] Separate **clinical safety** from **IT**. Patients in clinic today still need a path of care. IT does not get to vanish into a server room without a clinical lead in the loop.
- [ ] If a ransom note is visible, photograph the screen. Do not type in the note. Do not click links in it. Do not power-cycle "to see if it helps" until someone has captured what is on the screen.

## 0:10–0:25 · Stop the bleeding (contain)

Goal: stop further spread without destroying evidence.

- [ ] Isolate obviously affected endpoints from the network (unplug ethernet / disable Wi-Fi). Do not reimage yet.
- [ ] Disable shared drives / VPN / remote-access tools if they are a likely path between sites.
- [ ] Leave one affected machine as-is for later imaging if you have anyone who can image. If you do not, still do not wipe it in hour one.
- [ ] Identify what is **still up**: phones, internet, EHR, email, badge system, backups.
- [ ] Write a one-line status: what is down, what is up, whether care can continue on paper.

Do not:

- Pay, negotiate, or "just ask what they want"
- Run random decryptors from the internet
- Blast a staff-wide "we got hacked" email from a possibly compromised mailbox

## 0:25–0:40 · People and comms

- [ ] Call the pre-agreed list only (see [roles](../tabletop/roles.md)). In this lab: Clinic Director, IT, Charge Nurse, Billing, and whoever holds cyber insurance.
- [ ] Use voice or a channel you believe is still clean (cell phones, not the clinic email if it is acting strange).
- [ ] Clinical lead decides: stay open on paper, divert, or close. IT does not make that call alone.
- [ ] One person owns external comms. Nobody else posts, emails patients, or talks to press.

Draft, do not send yet, a two-sentence internal note:

```
Scheduling and some workstations are down. We are containing a suspected incident.
Use paper fallback. Do not try to "fix" a PC that shows a note. Call [IC] with anything new.
```

## 0:40–1:10 · Backup truth and evidence

Ask these out loud. Write the answers. Guessing is how you restore the infected copy.

- [ ] Last **successful** backup of EHR / scheduling / file shares: date, time, destination.
- [ ] Is there an **offline** copy (USB, cloud immutability, tape, vendor backup) that was not mounted this morning?
- [ ] Has anyone plugged the USB "home copy" into a possibly affected PC today? If yes, treat it as suspect.
- [ ] Last time a restore was **tested**: date, or "never."
- [ ] Vendor status: EHR host (cloud vs on-prem). If cloud, call the vendor. If on-prem, do not power the server back and forth.
- [ ] Preserve: ransom note photo, list of affected hostnames, last-good backup ID, firewall / NAS logs if you can export them without installing new tools in a panic.

## 1:10–1:40 · Decide the next 24 hours

IC + Director, in one sitting:

1. **Care:** open / divert / close for the rest of today.
2. **Restore vs rebuild:** do we even have a last-known-good, or are we on paper until a vendor lands?
3. **Help:** insurance, IR firm, EHR vendor, MSP. Call the one that already has a contract. Hour two is late to start shopping.
4. **Legal / privacy:** if patient data may be involved, legal gets a factual summary, not a theory. Do not notify patients in hour two unless counsel says so. Wrong notice is its own incident.
5. **Ransom:** default is do not pay. That decision belongs to leadership + legal + insurance, not IT in a hallway.

Write the decisions in the log. If it is not written, it did not happen.

## 1:40–2:00 · Hand-off

- [ ] 10-line status for anyone joining: what happened, what's down, what's contained, backup truth, open decisions, who is IC through tonight.
- [ ] Staffing: who stays, who goes home, who is on call at 18:00.
- [ ] Next checkpoint time (example: 10:40). Do not dissolve into "we'll see."

## Out of scope for hour two (on purpose)

Malware family, decryptor shopping, full forensics, patient notification letters, press. Those eat the clock. They belong after containment and after someone who does this for a living is on the phone.
