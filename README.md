# RAUM

**Translates. Checks. Forgets.**

RAUM is a private AI interpreter that lives in the room. It translates between two people who do not share a language while they are still talking, checks every translation before anyone acts on it, and writes the minutes. Every model runs on one box on the table, so no audio, text or translation is sent to a third party.

**Landing page: https://raum-web.vercel.app**

> **RAUM is not open source.** This repository is an overview only and contains no RAUM code. The landing page and the product are closed source and all rights are reserved.

## What it is for

Conversations where a leak is a legal problem, and where a wrong number is a real harm.

| Room | People | What RAUM guards |
|---|---|---|
| Sprechzimmer | Doctor and patient | Doses, allergies, a take-home summary in the patient's language |
| Kanzlei | Lawyer and client | Deadlines and dates, plain-language explanations the lawyer approves |
| Verhandlungsraum | CEO and foreign partner | Every price offered, minutes both sides approve |

Everyone joins on their own phone by scanning a QR code and hears the other person in their own language.

## Private

- **Everything runs on the box.** Speech recognition, translation, the check and the voice are models running on one machine in the room. Nothing leaves it.
- **Nothing is kept.** Sessions are encrypted with a key held only in memory. Burn destroys the key.
- **An audit trail without the content.** A hash-chained log records what happened, never what was said.
- **Why it has to be local.** Doctors and lawyers are bound by professional secrecy, and companies must actively protect trade secrets. A cloud interpreter is a disclosure.

## Fast

Measured on the reference box (ASUS Ascent GX10, NVIDIA GB10), warm:

| Step | Time |
|---|---|
| First words | 677 ms |
| A full sentence | 888 ms |
| Spoken voice | 1399 ms |
| The check | 1425 ms |

On real phones the voice arrives at a median of 0.82 to 1.03 seconds. The fact guard, which verifies numbers, doses, dates and amounts in code, takes 0.2 ms and caught 100 % of the errors with no false alarms on a 90-record evaluation.

## How it checks

Any AI can translate. RAUM checks. Code verifies numbers, doses, dates and names. A second model from a different family translates the result back, and the meanings are compared. If something is unclear, RAUM asks a spoken yes or no question before anyone acts on it.

## Built at

The Macromedia Berlin Hackathon, 2 to 3 November 2026.

## Licence

Not open source. Copyright the RAUM team. All rights reserved. Nothing in this repository grants any licence to the RAUM software, its models' configuration, its design or its landing page.
