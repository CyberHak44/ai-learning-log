# Auditing a small firm, starting with my own

Status: round 1 done 2026-11-05. Method published in the [SME security audit toolkit](https://github.com/CyberHak44/sme-security-audit-toolkit). Findings from any real audit, including my own, are confidential and never published.

## The question

How do you audit a founder-led firm honestly, in a way the owner can act on, and stop the fixes slipping once the report is filed?

## Why it matters

Small firms are now asked the same questions as large ones: bank vendor questionnaires, tender security schedules, ISO 27001 requirements passed down the supply chain. Most cannot answer them with evidence. And in founder-led firms, the failures that hurt first are rarely hackers. They are missed dates: a lapsed licence, late accounts leading to a strike-off notice, insurance that quietly expired.

## The method

| Move | What happens | GRC term | Where it is defined |
| --- | --- | --- | --- |
| 1 Scope | Every legal entity and every trading name | Scope of the management system | ISO/IEC 27001 clause 4.3 |
| 2 Tailor | 42 controls, tagged by jurisdiction, buyer type, service type and size; untagged controls score NA, never deleted | Statement of Applicability | ISO/IEC 27001 clause 6.1.3 |
| 3 Evidence first | Registry records, filing history, public DNS, the document register; interview only for what evidence cannot show | Audit evidence | ISO 19011 |
| 4 Score | G evidenced, A partial or owner's word only, R none, failed or overdue | Conformity | ISO 19011 |
| 5 Grade | Critical (cannot trade or deliver), High (blocks a regulated buyer), Medium, Low | Risk evaluation | ISO/IEC 27005 |
| 6 Fix | One fix per gap, with cost tagged certain, likely or guessing, an owner and a week | Risk treatment plan | ISO/IEC 27001 clause 6.1.3 |
| 7 Plan | Fixes enter the client's existing plan by severity; no new hours unless agreed | Planning to achieve objectives | ISO/IEC 27001 clause 6.2 |
| 8 Keep | Renewal register, reminders at 60, 30 and 7 days, weekly line, monthly re-score | Monitoring and continual improvement | ISO/IEC 27001 clauses 9.1 and 10.1 |

## Thrashing it out

Hakim takes a position, Polly, my AI assistant, challenges it, and we record where we landed. Nothing here is final.

| # | Position (Hakim) | Challenge (Polly) | Where we landed |
| --- | --- | --- | --- |
| 1 | Score it harshly: if it hurts, it is real | Harsh scores can demoralise an owner and lose the sale | Harsh and evidence-based, but always shown with the fix, the cost and the week, and re-scored monthly so the owner sees the reds fall. The first score is the starting line, not the verdict |
| 2 | Put the audit in the public repo | A public list of a firm's own gaps is a target list for attackers, and a buyer's assessor will find it | The method, the control library and the blank workbook are public. Every completed audit stays in the client's controlled folder |
| 3 | We need measures so it does not slip | Willpower is not a control | Six habits: a renewal register, calendar reminders at 60, 30 and 7 days, a daily start-of-day check, a weekly scorecard line, an escalation rule that gives red dates a fixed daily block, and a monthly re-score with statutory filings handed to one accountant |
| 4 | Audit my own group before selling it | Self-audits are soft, because you mark your own homework | The evidence rule removes the softness: the owner's word never scores green. Client zero is also the sales answer to "what did you find in your own firm?" |

## Controls checklist

- [ ] Every legal and commercial date on one register, with reminders at 60, 30 and 7 days
- [ ] MFA with an authenticator app or key on every account that touches company or client data
- [ ] Credentials in a password manager; nothing emailed or reused
- [ ] Devices encrypted (BitLocker), patched and protected, with status screenshots on file
- [ ] SPF, DKIM and an enforced DMARC policy on every domain, sending or not
- [ ] Backups independent, encrypted and restore-tested each quarter
- [ ] Every public claim on the website evidenced, or removed

## Study page

[Secure your own firm](https://cyberhak44.github.io/ai-learning-log/dashboards/secure-your-own-firm.html): nine steps with diagrams and a self-test, from the audit loop to BitLocker and DMARC.

## Open questions

- Which controls should a UAE free zone company add for its own registry and immigration obligations, and how do they differ between free zones?
- At what size does a firm need Cyber Essentials Plus rather than the self-assessed level?

## Sources

- [ISO 19011:2018 Guidelines for auditing management systems (ISO)](https://www.iso.org/standard/70017.html)
- [Google Workspace: set up DKIM (Google)](https://support.google.com/a/answer/174124)
- [Google Workspace: set up DMARC (Google)](https://support.google.com/a/answer/2466580)
- [BitLocker overview (Microsoft)](https://learn.microsoft.com/en-us/windows/security/operating-system-security/data-protection/bitlocker/)
- [Cyber Essentials (NCSC)](https://www.ncsc.gov.uk/cyberessentials/overview)
