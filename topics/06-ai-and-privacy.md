# AI and privacy

Status: round 1 started 2026-11-04. Filled in as we go.

## The question

When microphones and AI are in cars, phones, speakers and meeting rooms, how is privacy protected, and where does it stop?

## Why it matters

Connected devices now listen by default. Mozilla's 2023 review of 25 car brands found every one failed its privacy tests. A passing remark recorded in a company car can resurface years later, out of context, and damage a person or a company. No conduct policy can stop the remark. Governance can stop the recording, the keeping and the retrieval.

## The scenario

Two executives drive along the Corniche in a company car. One makes an offhand personal remark. The car's voice assistant and telematics are on. Who holds that audio, for how long, who can retrieve it, and what happens if it leaks?

## How GRC defines it

| What happens | GRC term | Where it is defined | The control |
| --- | --- | --- | --- |
| The car records the cabin | Data minimisation and purpose limitation | UAE PDPL; GDPR Article 5 | In-cabin audio off on fleet cars; collect only what the stated purpose needs |
| It is a company car | Controller, processor and transparency | UAE PDPL; GDPR | Fleet safety and location tracking do not justify recording conversations |
| Before connected fleets go live | Data protection impact assessment (DPIA) | GDPR Article 35; good practice under the PDPL | Run one before choosing a fleet or enabling features |
| The carmaker holds the data | Third-party (supplier) risk | ISO/IEC 27001 Annex A 5.19 to 5.22 | Supplier assessment and a data processing agreement: what, where, who, how long |
| Conversations in the car are sensitive | Information classification | ISO/IEC 27001 A 5.12 | Treat vehicle cabins like meeting rooms: confidential, no recording |
| Privacy is an afterthought | Privacy by design and by default | GDPR Article 25; ISO/IEC 27001 A 5.34; ISO/IEC 27701 | Microphones off by default, on-device processing, deletion by default |
| Kept for years | Retention and deletion | ISO/IEC 27001 A 8.10 | Short retention schedule with automatic deletion |
| A remark topples a CEO | Reputational and key-person risk | Enterprise risk register | Recorded with an owner, likelihood and impact |

GRC does not police manners; conduct belongs to HR policy. GRC makes sure a moment is not captured and stored without anyone deciding it should be. Data that was never kept cannot leak.

## Thrashing it out

Hakim takes a position, Polly, my AI assistant, challenges it, and we record where we landed. Nothing here is final.

| # | Position (Hakim) | Challenge (Polly) | Where we landed |
| --- | --- | --- | --- |
| 1 | Listening devices are everywhere; where does it stop? | It will not stop by banning devices | Three lines: law (consent and lawful basis under the PDPL), design (on-device processing, microphones off by default, short retention), and organisation (no sensitive conversations in connected cars or near smart speakers, as phones are kept out of board rooms) |
| 2 | At least 20 percent of life must stay private in the age of AI | Twenty percent of what? A percentage cannot be audited | A defined private-by-default zone that can be tested: health, faith, children, and private conversations at home and in vehicles are never collected or processed |
| 3 | An offhand remark between consenting adults cannot be policed | Agreed: the remark is not the control point | Control capture, retention and retrieval, not speech |
| 4 | What is the argument for recording every conversation? | The strongest case: regulators require it for trading lines, evidence protects the innocent, surveillance catches fraud and harassment, people behave better when recorded, and AI turns meetings into notes | Record by purpose, never by default. Record where the law requires it, where safety requires it, or where both parties agree for a stated reason, with notice, short retention and controlled access. Everywhere else the default is not recorded. Every recording is a liability: it can be breached, demanded in a lawsuit, or requested by the person it is about |
| 5 | How do you reassure a bank, or a CEO guarding a secret recipe, that documents read by a local AI never reach the cloud? | Promises fail with exactly the people who matter. Reassurance has to be something they can verify themselves | Give control and evidence, not assurances: the box sits in their building, encrypted with their keys, behind their firewall with outbound internet blocked; pull the network cable in the demo and it still answers; their own logs show zero outbound connections; no standing vendor remote access; a verifiable open-weight model with signed software; their red team is invited to test it. They choose what it reads, it respects existing permissions, and the crown jewels never have to go in. Residual risks stated openly: authorised users, updates, physical theft |

## Draft templates

The [templates](../templates/README.md) folder turns this subject into a transport policy, a vendor checklist, a leadership report and an executive briefing, each open to challenge.

## Voices from the field

- Eric Leandri, CEO of Aleria, argued on a panel at Make it in the Emirates that a minimum share of life, around 20 percent, must remain private in the age of AI.

## Controls checklist

- [ ] In-cabin audio and voice assistants off by default on fleet vehicles
- [ ] DPIA before deploying connected vehicles or meeting-room AI
- [ ] Connected device suppliers inside third-party risk scope, with data processing agreements
- [ ] Vehicle cabins and meeting rooms classified as confidential spaces
- [ ] Retention schedule with automatic deletion for any audio or transcripts

## Open questions

- Which UAE provisions apply to recording private conversations, and how do they treat company-owned spaces?
- What can a buyer realistically verify about where a carmaker sends voice data?

## Sources

- [Mozilla review: 25 car brands failed basic privacy tests, 2023 (Engadget)](https://www.engadget.com/tesla-tops-mozillas-list-of-creepiest-carmakers-but-25-brands-failed-basic-data-privacy-tests-202017058.html)
- [Schneier on Security: cars have terrible data privacy](https://www.schneier.com/blog/archives/2023/09/cars-have-terrible-data-privacy.html)
- [Make it in the Emirates 2026 (WAM)](https://www.wam.ae/en/article/177cudj-largest-ever-make-the-emirates-opens-abu-dhabi)
