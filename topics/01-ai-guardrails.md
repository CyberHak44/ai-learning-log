# AI guardrails

Status: round 1 complete, 2026-11-03. Filled in as we go.

## The question

What stops an AI tool from leaking data, being tricked, or doing something nobody intended?

## Why it matters

A business that adds AI to email, documents or customer chat adds a new way in for attackers and a new way out for data. Guardrails are the controls that keep the benefit and remove most of the risk.

## What we know so far

- The OWASP Top 10 for Large Language Model Applications (2025) lists the main risks, including prompt injection (LLM01), sensitive information disclosure (LLM02), improper output handling (LLM05) and excessive agency (LLM06).
- Prompt injection means hidden instructions in a web page, email or document that the AI reads and follows. It cannot be fully prevented today, so the design has to limit what a tricked AI can do.
- Guardrails sit in three places: what goes in (data the AI may see), what the AI may do (tools and permissions), and what comes out (checked before it is used or sent).

## Thrashing it out

Hakim takes a position, Polly, my AI assistant, challenges it, and we record where we landed. Nothing here is final.

| # | Position (Hakim) | Challenge (Polly) | Where we landed |
| --- | --- | --- | --- |
| 1 | Guardrails rest on ethics, data sovereignty and privacy, within local and international law | Ethics stops misuse but not the honest mistake: staff pasting client data into a free AI tool breaches the UAE PDPL with no bad intent | Four layers: purpose (lawful and authorised), data (classified, confidential data on business plans or local models), design (safe path by default), oversight (a named human approves irreversible actions) |
| 2 | The honest mistake is stopped by education: monthly case studies, fact-checking AI, asking how certain an answer is, critique loops | Training fades. Without system controls it relies on people remembering | Education plus design: managed AI accounts, consumer AI blocked, DLP, logs. People are trained to question AI. The system catches what they miss |
| 3 | Know your client: map the law to the client, and design to the strictest standard | GDPR follows where people are located and where you trade, not nationality | Map each client's law by establishment, where its data subjects are and its sector (PDPL, DIFC, ADGM, health, CBUAE, GDPR where it reaches). Default to the strictest standard that applies |
| 4 | Offensive tools need an IT policy with levels of authorisation; verify who is asking, not what is asked | To an AI, a pen test and an attack look the same. Accounts can be phished | Authorisation over content: phishing-resistant MFA, role-based access, a signed scope letter for offensive work, two-person approval for high-risk actions |
| 5 | If AI does everything, where does it stop? | Accountability needs legal personhood, and AI has none | AI works in the prep zone. A named person commands the action zone: sends, payments, deletes, publishing, configuration changes |

Round 1 completed 2026-11-03.

## How I apply it

- _to fill_: the rules I give each SME client before switching an AI assistant on.
- _to fill_: how the same rules map to ISO/IEC 27001 controls.

## Controls checklist

- [ ] Decide what data each AI tool may see, and keep confidential work on a local model
- [ ] Give AI tools the least access they need, one permission at a time
- [ ] Treat anything the AI reads from the web or email as untrusted
- [x] A person checks AI output before it is sent, published or acted on
- [x] Log what AI tools do, so actions can be traced
- [ ] Phishing-resistant MFA on every account that can use AI tools or approve actions

## Open questions

- How do you test a guardrail without real attackers?
- What should a 6-person business actually be told on day one?

## Sources

- [OWASP Top 10 for LLM Applications 2025, practical guide (Gravitee)](https://www.gravitee.io/blog/owasp-top-10-for-llm-applications-2025-a-practical-guide)
- [OWASP Top 10 LLM risks explained (Outpost24)](https://outpost24.com/blog/owasp-top-10-llm-risks-explained/)
