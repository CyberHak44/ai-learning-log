# AI-assisted security: how I work and what I'm learning

A working log of how I use AI tools in governance, risk and compliance (GRC) and security work, and what I learn each week. Every entry links to something you can check.

## How I use AI tools

| Tool | What I use it for | Status |
| --- | --- | --- |
| Polly, my AI assistant | Research, first drafts of crosswalks and briefs, pair-building [grc-workbench](https://github.com/CyberHak44/grc-workbench) step by step (I write and commit the code) | In use |
| Docker and Gordon | Packaging tools so every client gets the same tested build; Gordon, Docker's built-in assistant, to learn and debug | Learning |
| Docker Model Runner | Running language models locally, so confidential documents are never uploaded to a cloud AI | Learning |
| Oxylabs | Collecting public web data for brand look-alike monitoring and tracking regulator publications | Learning |

## Subjects I'm working through

Each subject is a working paper. I take a position, Polly, my AI assistant, challenges it, and the page records where we landed, the evidence, and the controls I would actually use. They start as frameworks and fill in over time.

| Subject | The question | Status |
| --- | --- | --- |
| [AI guardrails](topics/01-ai-guardrails.md) | What stops an AI tool leaking data, being tricked, or doing something nobody intended? | Round 1 done |
| [Agentic AI and human oversight](topics/02-agentic-ai-and-human-oversight.md) | When AI takes actions on its own, where must a person step in? | Framework |
| [The AI tools compared](topics/03-ai-tools-compared.md) | Polly (my AI assistant), Cursor, Grok, Gemini, Copilot: which tool for which job, and where does the data go? | Framework |
| [AI as a force multiplier](topics/04-ai-as-a-force-multiplier.md) | Where does AI really let one person do the work of several? | Framework |
| [AI governance frameworks](topics/05-ai-governance-frameworks.md) | ISO/IEC 42001, NIST AI RMF, the EU AI Act and CBUAE guidance, and how they fit with ISO 27001 | Round 1 started |
| [AI and privacy](topics/06-ai-and-privacy.md) | With microphones in cars, phones and rooms, how is privacy protected, and where does it stop? | Round 1 started |

## Dashboards I've built

Interactive study pages with diagrams and self-tests. Click to open them live in your browser:

| Dashboard | What it teaches |
| --- | --- |
| [ISA/IEC 62443 for building systems](https://cyberhak44.github.io/ai-learning-log/dashboards/iec62443-study.html) | Zones and conduits, security levels, the seven foundational requirements, the risk workflow |
| [Fortinet FortiGate essentials](https://cyberhak44.github.io/ai-learning-log/dashboards/fortinet-nse4-study.html) | Policies, NAT, security profiles, SSL inspection, IPsec VPN, hardening |
| [Docker, Gordon and local AI](https://cyberhak44.github.io/ai-learning-log/dashboards/docker-gordon-study.html) | Containers, Compose, the MCP Toolkit, running AI models locally |
| [Web data and the law](https://cyberhak44.github.io/ai-learning-log/dashboards/web-data-study.html) | Proxies, scraping APIs, brand look-alike monitoring, the UAE PDPL line |

Also built: [grc-workbench](https://github.com/CyberHak44/grc-workbench), a browser-based GRC tool. More detail in [dashboards](dashboards/README.md).

## Rules I work to

1. A person reviews and signs off everything that leaves my desk. AI drafts; I decide.
2. No client data goes into a cloud AI tool without the client's agreement. Confidential work runs on local models.
3. Public data only, within each site's terms. No personal data collected, no logging in where I am not authorised, no scanning or testing without written permission.
4. Every figure and quote is checked against a source before it is used.

## Learning log

| Date | Topic | What I learned | Proof |
| --- | --- | --- | --- |
| 2026-10-28 | IEC 62443 for building systems | An ISO 27001 ISMS fully covers 15 of 31 building-OT requirements I mapped; the gaps are scope, safety-based risk, target security levels per zone and unowned remote access | [iec62443-building-ot-crosswalk](https://github.com/CyberHak44/iec62443-building-ot-crosswalk) |
| 2026-10-28 | CBUAE operational risk regulation | ISO 27001 fully covers 16 of 39 cyber requirements; the 4-hour notification clock and Critical Operations mapping have no ISO equivalent | [cbuae-orm-cyber-crosswalk](https://github.com/CyberHak44/cbuae-orm-cyber-crosswalk) |
| 2026-10-29 | Building a GRC tool with AI | Pair-building six stages with an AI assistant: asset and risk registers, Statement of Applicability, supplier scoring, CBUAE readiness and a one-page gap report | [grc-workbench](https://github.com/CyberHak44/grc-workbench) |
| 2026-10-30 | ISA/IEC 62443 fundamentals | Zones and conduits, security levels SL 1 to 4 sized to the attacker, the seven foundational requirements, and the 3-2 risk workflow | Study notes |
| 2026-11-02 | Fortinet FortiGate (NSE 4 track) | Policies are first-match top-down with an implicit deny; NAT and Virtual IPs; why deep SSL inspection matters; hardening the firewall itself maps to ISO 27001 controls | Study notes |
| 2026-11-02 | Docker, Gordon and local AI | Images vs containers, ports and volumes, Compose for multi-part services, least-privilege tool access through the MCP Toolkit, and running models locally | Study notes |
| 2026-11-02 | Web data and the law | How proxies and scraping APIs work, and where the UAE PDPL draws the line: no "legitimate interests" basis, so no harvesting personal data | Study notes |
| 2026-11-03 | AI guardrails and agentic AI | Started five working papers: guardrails, human oversight of AI agents, the main AI tools, AI as a force multiplier, and AI governance frameworks | [topics](topics/) |
| 2026-11-03 | AI guardrails, round 1 | Authorisation beats content filtering; AI preps, people act. Jurisdiction follows where people are and where you trade, not nationality | [01-ai-guardrails](topics/01-ai-guardrails.md) |
| 2026-11-04 | Zero trust, speed and privacy | Zero trust is not zero autonomy; the risk is complacency. Liability, procurement and insurance make insecurity cost more than being second. Control capture and retention, not speech | [01](topics/01-ai-guardrails.md), [05](topics/05-ai-governance-frameworks.md), [06](topics/06-ai-and-privacy.md) |

## Author

**Clive (Hakim) Bean**: ISO/IEC 27001 Lead Auditor (GRC Mastery, 2026, Credly-verified). Intelligent Environments L.L.C-FZ, Abu Dhabi.
