# AI guardrails

Status: framework, 2026-11-03. Filled in as we go.

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

| # | Position | Challenge | Where we landed |
| --- | --- | --- | --- |
| 1 | Guardrails slow people down | They only need to stop the few actions that cannot be undone; everything else runs freely | _to fill_ |
| 2 | _to fill_ | _to fill_ | _to fill_ |
| 3 | _to fill_ | _to fill_ | _to fill_ |

## How I apply it

- _to fill_: the rules I give each SME client before switching an AI assistant on.
- _to fill_: how the same rules map to ISO/IEC 27001 controls.

## Controls checklist

- [ ] Decide what data each AI tool may see, and keep confidential work on a local model
- [ ] Give AI tools the least access they need, one permission at a time
- [ ] Treat anything the AI reads from the web or email as untrusted
- [ ] A person checks AI output before it is sent, published or acted on
- [ ] Log what AI tools do, so actions can be traced

## Open questions

- How do you test a guardrail without real attackers?
- What should a 6-person business actually be told on day one?

## Sources

- [OWASP Top 10 for LLM Applications 2025, practical guide (Gravitee)](https://www.gravitee.io/blog/owasp-top-10-for-llm-applications-2025-a-practical-guide)
- [OWASP Top 10 LLM risks explained (Outpost24)](https://outpost24.com/blog/owasp-top-10-llm-risks-explained/)
