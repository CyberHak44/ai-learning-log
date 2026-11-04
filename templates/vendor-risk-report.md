# Vendor risk report for leadership

Draft v0.1 for discussion, 2026-11-04. Format for presenting a vendor review to executives and the board. Most executives read only page one, so it must stand alone. The example below is fictional.

## Page 1: summary

| Field | Example |
| --- | --- |
| Vendor | Example Transport Co (fictional) |
| Assessment date | [date] |
| Overall rating | Medium, pending one technical fix |
| Business impact | High: the vendor will carry executives who handle confidential information |

| Risk area | Before fixes | After fixes | Decision needed |
| --- | --- | --- | --- |
| Legal and contractual | Low | Low | None |
| People | Low | Low | None |
| Technology and privacy | High | Low | Approve onboarding only after microphones are verified disabled |
| Operations | Medium | Low | None |

**Summary.** The vendor meets most requirements. One finding is critical: its vehicles record cabin audio to a cloud service by default. Onboard only after interior microphones are physically disabled and this is verified.

## Page 2: findings

**Finding 1: cabin audio recorded to the cloud (critical)**
- What we found: dashcams record cabin audio by default and upload it to the camera provider's cloud.
- Why it matters: a remark such as "Bob is a jerk, we are letting him go next week" would sit on an unvetted third-party server, where it could be leaked, requested or quoted out of context.
- Fix: vendor signs a hardware attestation that cabin microphones are disconnected on every vehicle assigned to us; we spot-check.

**Finding 2: drivers' personal devices (medium)**
- What we found: drivers carry personal phones and smartwatches.
- Why it matters: consumer apps can pick up audio and location.
- Fix: personal devices in a locked pouch; company phone for navigation.

## Page 3: actions

| # | Action | Owner | Deadline |
| --- | --- | --- | --- |
| 1 | Contract clause: deploying a vehicle without verified microphone removal is a breach | Legal and procurement | Before signature |
| 2 | Unannounced vehicle checks | Security | Within 30 days of start |
| 3 | Sign off residual risk | CISO | After evidence received |

## Thrashing it out

| # | Draft said | Challenge | Where we landed |
| --- | --- | --- | --- |
| 1 | Named a fictional vendor with a realistic name | Could match a real company | "Example Transport Co (fictional)" |
| 2 | Example remark: "Bob is a jerk" | Is an insult about a named employee too informal for client material? | Kept, deliberately. It is a mild stand-in; real remarks are usually far worse. A remark like this, recorded, can cost someone a job or start a disciplinary process. Privacy protects Bob as well as the speaker: what is never recorded cannot reach him. And if a recording does exist, Bob may be able to request it as personal data about him, so recording creates risk for everyone |
| 3 | "Meets 85 percent of requirements" | A percentage hides which controls failed | Lead with the critical finding and the decision needed |
