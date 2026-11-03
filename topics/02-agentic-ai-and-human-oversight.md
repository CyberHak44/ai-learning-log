# Agentic AI and the need for a human in the loop

Status: framework, 2026-11-03. Filled in as we go.

## The question

When an AI can take actions on its own (send, buy, delete, change systems), where must a person step in?

## Why it matters

Agentic AI moves from answering questions to doing work: running commands, editing files, sending messages. The risk is no longer a wrong answer but a wrong action. Regulators and auditors will ask who approved it.

## What we know so far

- "Human in the loop" means a person approves each important action. "Human on the loop" means the AI acts and a person monitors and can stop it.
- The EU AI Act requires human oversight for high-risk AI systems (Article 14). After the Digital Omnibus, adopted on 29 June 2026, most high-risk obligations moved to 2 December 2027.
- Coding agents now run in parallel and in the background. Cursor, for example, runs several agents at once and lets teams add hooks that block unsafe tool calls before they run.
- In my own work with Polly, my AI assistant, irreversible actions (deleting, sending, publishing, pushing code, spending money) need my explicit approval every time. That rule is the guardrail in practice.

## Thrashing it out

Hakim takes a position, Polly, my AI assistant, challenges it, and we record where we landed. Nothing here is final.

| # | Position | Challenge | Where we landed |
| --- | --- | --- | --- |
| 1 | Approve everything | Approval fatigue: people click yes without reading. Approve only what cannot be undone | _to fill_ |
| 2 | _to fill_ | _to fill_ | _to fill_ |
| 3 | _to fill_ | _to fill_ | _to fill_ |

## How I apply it

- _to fill_: my approval rules, written as a one-page policy a client can adopt.
- _to fill_: which tasks I let an agent run unattended, and which never.

## Controls checklist

- [ ] List the actions an agent may never take alone (send, pay, delete, publish, change access)
- [ ] Every agent action is logged with who approved it
- [ ] There is a stop button, and someone owns it
- [ ] Agents run with their own limited accounts, never an admin account

## Open questions

- How do you keep approvals meaningful when there are hundreds a day?
- Who is accountable when an approved agent action goes wrong?

## Sources

- [EU AI Act high-risk deadline moved to December 2027 (Cloud Security Alliance)](https://labs.cloudsecurityalliance.org/research/csa-research-note-eu-ai-act-omnibus-vii-deadline-delay-20260/)
- [Cursor: from editor to agent workspace (S. Dubois, updated Oct 2026)](https://www.dsebastien.net/cursors-last-six-months-from-editor-to-agent-workspace/)
