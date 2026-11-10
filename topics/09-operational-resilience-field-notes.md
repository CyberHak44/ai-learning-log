# Operational resilience: field notes from a UAE banking forum

Status: round 1 drafted, 2026-11-10. Filled in as we go.

## The question

What are UAE bank security leaders actually worried about after the March 2026 cyber wave, and what does it mean for how firms of any size plan to keep running?

## Where these notes come from

My notes from the UAE Banking Cybersecurity and Resilience Forum, Abu Dhabi, 9 November 2026. Points are summarised by theme and not attributed to individual speakers. Interpretations and challenges are mine, worked through with Polly, my AI assistant.

## What I heard: seven themes

1. **The security leader's job is proving trust.** Not just protecting systems, but proving digital trust to customers, clients, regulators and the board.
2. **Time has compressed.** Work that once took six months to identify and plan now has to happen close to real time. Testing quarterly or even monthly is too slow. AI is moving faster than banks can adopt it, and the old methods will not solve the new problems.
3. **Attackers log in rather than break in.** Identity is the new perimeter. Phishing remains the number one risk, and capable AI models, including open-weight ones anyone can download, are scaling the volume of attacks.
4. **Assume breach, and know your minimum.** It is a matter of when, not if. Know the kill chain, segment the network, and define the minimum service you must keep running rather than shutting everything down. Encrypt what matters most, and protect the keys as well: in the cloud, your data sits on someone else's infrastructure.
5. **Documented resilience is not actual resilience.** What a bank believes it has on paper often differs from what is really in place: how fast it can patch, what it actually monitors, and whether dashboards reflect the customer's real experience. Controls should scale with value: a small payment and a very large one should not get the same checks.
6. **One team.** Fraud, anti-money laundering, security, application development, IT and cyber often work in silos. They need to act as one team with one voice.
7. **Agentic AI breaks traditional controls.** Traditional controls assume predictable execution. AI agents act dynamically, which exposes them to prompt injection. Guardrails must be ones an agent cannot bypass, data must be classified before an agent can reach it, and identity checks now have to answer a new question: is this a human or an AI?

## Key idea: minimum viable company

The minimum viable company (MVC), also called minimum viable business, is industry language used by large consultancies and backup vendors, not an ISO term. KPMG describes it as the minimum set of capabilities, data, technology, people and third parties an organisation needs to keep operating in a crisis, especially when critical digital services are compromised.

How it fits with business continuity terms:

- **Minimum business continuity objective (MBCO)** is the floor: the least service you must keep delivering.
- **Minimum viable company** is the kit list behind that floor: people, processes, technology, data, facilities and suppliers. It is also your restore order after an attack.

Memory hook: MBCO is the floor, the MVC is the kit list behind it.

For a small firm the same idea becomes one question: "If your systems went down tomorrow, what is the least you would need to keep trading?"

## Thrashing it out

I take a position, Polly challenges it, and the page records where we landed. Nothing here is final.

| # | Position (Hakim) | Challenge (Polly) | Where we landed |
| --- | --- | --- | --- |
| 1 | Assume breach and define the minimum you must keep running | Most firms have never written that minimum down, so "assume breach" stays a slogan | Write the minimum viable company down before an incident: services, people, data, systems, facilities and suppliers, in restore order. Test it once a year |
| 2 | Documented resilience is not actual resilience | Then a paper audit proves little | Audit evidence, not documents: patch times measured, restores tested, monitoring shown working. No evidence scores red |
| 3 | Attackers log in rather than break in | Then the strongest control is on identity, not the network edge | Phishing-resistant MFA, least privilege and fast removal of leavers come before any new firewall spend |
| 4 | Agentic AI breaks traditional controls | Asking an agent to behave is not a control | Guardrails outside the agent: permissions it cannot change, classified data it cannot reach, and a named human approving irreversible actions. Links to [agentic AI and human oversight](02-agentic-ai-and-human-oversight.md) |
| 5 | Silos between fraud, AML and cyber leave gaps | One team is an organisation chart problem, not a technology one | Shared incident playbooks and one risk register across fraud, AML and cyber, even when the teams stay separate |

## How I apply it

- In the Business Security Audit for small firms: add the minimum viable company question and score whether it is written down and tested. See [auditing a small firm](07-auditing-a-small-firm.md).
- For regulated clients: map the minimum viable company to the CBUAE Operational Risk Management Regulation's critical operations, which must be mapped to their people, technology, data, facilities and third parties.

## Controls checklist

- [ ] Minimum viable company written down: services, people, data, systems, facilities, suppliers
- [ ] Restore order agreed and tested at least once a year
- [ ] Encryption keys held and protected separately from the data they protect
- [ ] Phishing-resistant MFA on every account that can move money or data
- [ ] One risk register shared by fraud, AML and cyber

## Open questions

- How small can a firm be before a written minimum viable company stops being worth the effort?
- How do you test "human or AI?" in identity checks without adding friction for real customers?

## Sources

- [KPMG: building technology resilience in an era of cyber instability](https://kpmg.com/uk/en/insights/advisory/building-technology-resilience-in-era-of-cyber-instability.html)
- [CBUAE Rulebook: Operational Risk Management Regulation](https://rulebook.centralbank.ae/en/rulebook/operational-risk-management-regulation)
- My own notes from the UAE Banking Cybersecurity and Resilience Forum, 9 November 2026
