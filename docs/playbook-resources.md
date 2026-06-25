# PCMH Product Development Resource Book

*Product Delivery Grounded in User Need, Powered by Modern Engineering*

!!! note "About this resource book"
    We exist for our users. Everything in this resource book flows from that. DHCW's purpose is to make digital a force for good in health and care. This document describes how the PCMH Product & Delivery Group puts that purpose into practice: the principles, delivery practices, tools, and reading that underpin the way we design, build, and run products for clinicians, patients, and the people of Wales.

**Why now:** The DHCW Organisational Strategy 2024–2030 sets out five missions that guide our work. PCMH's products directly support Mission 2 (delivering high-quality digital products and services), Mission 3 (expanding the digital health and care record), and Mission 4 (driving better value and outcomes through innovation). We're entering a period where AI-assisted development, modern quality engineering, and data readiness are reshaping how we deliver against those missions. This book gives you the context to engage with that work confidently.

**How to use it:** You don't need to read every link. Start with the sections relevant to your role, and use the "Start Here" resources as entry points. Come back to the rest when you need it.

---

## 1. Product, User-Centred Design, and How We Work

Before we talk about AI, branching strategies, observability, or any of the tooling in this book, we need to be clear about the foundation everything else sits on. DHCW's first strategic principle is putting people first. That means everything we design, build, and maintain must be grounded in user need. That is the starting point, not an afterthought. Every technology decision, every architectural choice, and every delivery practice in this resource book exists to serve that principle. Our delivery model is continuous delivery: small, frequent, safe releases that get value to users as quickly as possible and give us fast feedback on whether we're building the right thing.

### User-Centred Design

We work closely with the User-Centred Design (UCD) team when needed, and that relationship is central to how we build products. User research, service design, interaction design, and accessibility are not stages that happen before or after engineering. They are woven into the way we think about what to build, who we're building it for, and whether it's working.

For product owners, this means user needs drive the backlog. For engineers, it means the interfaces you build must reflect research, not assumptions. For delivery managers, it means protecting the space for user research and usability testing within the delivery cadence, rather than treating them as nice-to-haves that get squeezed out when time is short.

Two commitments deserve explicit mention:

- **Welsh and English by default.** As a Welsh public body delivering the Digital Service Standard for Wales, our products must be designed in Welsh and English from the outset, not retrofitted. This applies to new builds, modernisations, and any user-facing changes.
- **Accessibility is a core design principle.** It is not a specialised testing concern. Every product we build must be usable by everyone who needs it, meeting WCAG standards and reflecting the diversity of our users across Wales.

**The design system:** DHCW is developing a design system that will become the foundation for everything we build. Once available, it will be the basis for all new product work across PCMH. Until then, we use the existing component library that is being fed into the design system. If you're building a new interface or modernising an existing one, use the component library. Don't invent your own patterns. Consistency matters for users, for accessibility, and for the long-term maintainability of our products.

!!! warning "AI-assisted development and clinical safety"
    When AI tools generate UI code, they need guardrails. The design system and component library are those guardrails. An AI agent that generates a form or a search interface should be working from the same patterns our designers have validated with users, not hallucinating its own component library. When AI is used in clinical contexts, we have an additional responsibility: to ensure that AI-generated code meets DCB0129 and DCB0160 clinical safety standards, and that data residency and privacy obligations are maintained. Innovation must not outrun governance.

### How We Work: The 9-Day Increment

PCMH product teams work in a 9-day increment cycle. This is live on some teams and rolling out to others. Each day of the increment provides 5 hours of increment-based work, with the remaining 2.5 hours the personal responsibility of the team member.

**The 5-hour increment day:** Every team member has 5 hours per day dedicated to increment work: building, testing, reviewing, deploying, and all the activities that move the product forward. This is protected, focused time. The increment aims to release as often as possible, safely and sustainably, within that 9-day window. Frequent, small releases are the goal, not a single batch at the end of the increment.

**The 2.5-hour personal responsibility window:** The remaining 2.5 hours each day belong to the team member. This time is for professional development, organisational improvement, community of practice participation, learning new tools, contributing to open-source work, and non-increment activities that make us better at what we do. This is not secondary work. It is part of the work. DHCW's strategy commits to an academy approach to developing people, and this protected time is how we honour that commitment at team level. Use it well.

!!! info "One exception"
    If our customers need us, they take priority. Service requests, live incidents, and urgent clinical needs come first regardless of what the increment plan says. That's non-negotiable. We build products for clinicians and patients, and their needs don't wait for our sprint boundaries.

### Products, Not Projects

DHCW is moving from projects to products. WCP, WIS, Choose Pharmacy, CDR: these are some examples of long-lived products with long-lived teams. That distinction matters because it changes how we think about investment, quality, and technical debt. A project team can defer quality and walk away. A product team lives with its decisions. This is why "you build it, you run it" is a core principle, and why the observability, quality, and branching practices later in this book aren't optional extras. They are the cost of running products responsibly. The single best indicator of whether a product team is doing this well is deployment frequency: how often can you safely put working software in front of users?

### Show and Tell: Closing the Loop with Users

Every product team must hold a public Show and Tell at the end of each increment to go back to users with the work that has been done. This is not optional and it is not a team-internal demo. It is an open session where clinicians, policy colleagues, Health Board stakeholders, and anyone with an interest in the product can see what has changed, ask questions, and tell us whether we're building the right thing.

We exist for our users, and we need to ensure what we are building is what they want. A Show and Tell is the simplest, most honest mechanism for doing that. It closes the feedback loop between delivery and need. It surfaces misunderstandings early, before they become expensive. And it builds trust, because working in the open means people can see what we're doing and hold us to account.

**What a good Show and Tell looks like:** Show working software, not slides. Demonstrate what users can now do that they couldn't before. Be honest about what didn't get done and why. Invite questions. Listen to the answers. Treat it as a research opportunity, not a presentation.

**Who should attend:** Everyone is welcome. Product owners should actively invite the users and stakeholders who will be most affected by the work shown. Engineers should present their own work. Delivery managers should track the feedback and make sure it feeds back into the next increment's priorities. If nobody from outside the team is attending your Show and Tell, something has gone wrong.

!!! note "The thread through this document"
    Every section that follows connects back to user need, the Digital Service Standard for Wales, and the commitment to working in the open. AI-assisted development (Section 3) is valuable because it lets us respond to user needs faster. Agentic quality engineering (Section 4) is valuable because it helps us catch problems before users do. Observability (Section 6) is valuable because it tells us what users are actually experiencing, not what we think they're experiencing. Branching and working agreements (Section 7) are valuable because they reduce the time between identifying a user need and delivering a response. And the Show and Tell is where all of that comes together: the moment we stand in front of the people we serve and show them what we've done. If a practice doesn't ultimately serve the people who use our products, we should question why we're doing it.

---

## 2. The Big Picture: What's Changing and Why It Matters

The landscape of product development is shifting faster than at any point in our careers. Gartner's 2026 strategic technology trends place agentic AI, domain-specific language models, and AI-native development platforms at the centre of enterprise strategy. This isn't future-gazing. It's happening now, and PCMH needs to be ready.

Three converging forces are driving this for us specifically:

1. **AI-assisted development is production-ready.** Tools like Claude Code and GitHub Copilot have matured to the point where engineers paired with AI are demonstrably more productive.
2. **Quality engineering is being reshaped.** The PACT framework (Proactive, Autonomous, Collaborative, Targeted) offers a structured way to evolve from testing-as-activity to agents-as-orchestrators. This aligns directly with our existing commitment to Bryan Finster's quality principles: quality is user-defined, build small and frequently, and "you build it, you run it."
3. **Data readiness is the bottleneck most organisations miss.** Gartner research found that only 32% of organisations with AI initiatives have a systematic data readiness process.

### Key Reading

**AI-Ready Data Essentials to Capture AI Value** *(Gartner)*
Gartner's five-step framework for data readiness. Start here if you want to understand why "high-quality data" doesn't automatically mean "AI-ready data."

**Ensure Your Data Is Ready for the Agentic AI Era** *(Gartner)*
The checklist referenced by the NICE/Gartner CX trends research. Practical guidance on what CX and IT leaders need to change to translate AI trends into measurable results. Gartner predicts that by 2028, 40% of agentic AI projects will be cancelled due to escalating costs, unclear business value, or inadequate risk controls.

**Gartner Top Predictions for Data & Analytics 2026** *(Gartner, March 2026)*
Key stat: by 2030, 50% of AI agent deployment failures will stem from insufficient governance and enforcement at runtime.

---

## 3. AI-Assisted Development: How We're Building Differently

AI-assisted development changes what engineers spend their time on rather than replacing them. The shift is from execution to direction, from writing code to reasoning about systems. Communication, the ability to distil domain knowledge into clear, structured prompts, becomes the critical skill. This directly supports DHCW's fourth mission: driving better value and outcomes through innovation.

This is good news for a team that includes delivery managers, analysts, and product owners alongside engineers. The gap between "I have an idea" and "I have a working thing" has collapsed. If you've ever written a good user story, a clear acceptance criterion, or a technical spec that a developer could actually use, you already know how to work in this world.

### The bdfinst/agentic-dev-team Plugin

We've evaluated the [bdfinst/agentic-dev-team](https://github.com/bdfinst/agentic-dev-team) Claude Code plugin, which implements a Research → Plan → Implement pipeline with human gates and inline review checkpoints. The key insight is task sizing: work should be decomposed into small, session-completable units. This aligns with our existing delivery principles around small batch sizes and frequent deployment.

### Tools & Resources

**[Claude](https://claude.ai)** *(Anthropic)*
Free tier available immediately. Use for reasoning about problems, drafting specs, analysing documents. No setup required.

**GitHub Copilot**
Licences issued for the team. IDE-integrated code completion and chat. Works across all our primary languages.

**[bdfinst/agentic-dev-team](https://github.com/bdfinst/agentic-dev-team)**
Claude Code plugin with Research → Plan → Implement pipeline. Human gates at each stage. We're evaluating this for the WIS team.

**[Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices)** *(Anthropic)*
Official guidance on CLAUDE.md files, context management, and getting the best results from AI-assisted coding.

---

## 4. Agentic Quality Engineering and the PACT Framework

Quality engineering is undergoing a fundamental shift. The [Agentic QE Framework](https://agentic-qe.dev), created by Dragan Spiridonov and available as open source, provides a structured model for evolving from testing-as-activity to agents-as-orchestrators. At its core is PACT: four principles for building explainable, autonomous quality systems.

| Principle | What it means |
|---|---|
| **Proactive** | Anticipate and prevent quality issues before they surface. Agents analyse codebases and find security issues, memory leaks, and anti-patterns before code runs. |
| **Autonomous** | Agents make decisions and take actions without constant human intervention, but they must explain their reasoning. Autonomy with explainability, not autonomy without accountability. |
| **Collaborative** | Human expertise and AI capabilities working together. Quality becomes a team sport. Agents augment expertise; they don't replace it. Every autonomous decision needs a reason. |
| **Targeted** | Focus efforts where they matter most. Risk-based, value-driven quality that delivers business impact. Coverage metrics give way to risk-targeted intelligence. |

**Why this matters for PCMH:** Our current WIS test coverage sits at 59% automated, with 40,000 tests running daily. The Agentic QE model doesn't ask us to throw that away. It asks us to evolve it: have agents find coverage gaps and prioritise by risk, detect and stabilise flaky tests, and learn our codebase patterns over time. This is an evolution, not a revolution.

**Connection to our quality principles:** Bryan Finster's "quality is user-defined" maps directly onto PACT's Targeted principle. "You build it, you run it" maps onto Autonomous. Small frequent delivery maps onto Proactive (catching problems early through continuous feedback). This is our existing philosophy with better orchestration, not a new one.

### The Agentic QE Fleet

The open-source [Agentic QE Fleet](https://github.com/agentic-qe/fleet) is a practical implementation of these principles. It coordinates 60 specialised agents across test generation, coverage analysis, security scanning, and chaos engineering. It works best with Claude Code and integrates with 11 coding agent platforms. Crucially, it includes human checkpoints at pre-deploy and security stages: exactly the kind of guardrails we need for clinical systems.

The fleet is organised into domains that map onto real delivery concerns: core testing (TDD in both London and Chicago schools, XP practices, risk-based testing), specialised testing (accessibility, security, contract testing, chaos engineering), and domain skills (test generation, coverage analysis, defect intelligence). For a team working on NHS clinical systems where DCB0129 and DCB0160 clinical safety standards apply, the explainability and audit trail capabilities are particularly relevant. The fact that accessibility testing is built into the agent fleet as a first-class concern, not an afterthought, also matters for a Welsh public body committed to the Digital Service Standard.

### Agentic QE Resources

**[Agentic QE Framework](https://agentic-qe.dev)**
The framework site. Start here for the conceptual foundation, PACT principles, and how classical QE bridges to autonomous systems.

**[Agentic QE Fleet](https://github.com/agentic-qe/fleet)** *(GitHub)*
Open-source implementation. 60 specialised agents, MCP server integration, works with Claude Code. Free to fork, build, and contribute.

**[What is Agentic QE? (And Why PACT Matters)](https://agentic-qe.dev/blog/what-is-agentic-qe)**
Dragan Spiridonov's deep-dive article. Real implementation stories, honest about failures, no vendor hype. The best single article to understand the PACT model.

**How AI Will Shape QA Leadership in 2026** *(Spiridonov, Xray)*
Covers the five fundamental shifts defining 2026 QA leadership, including orchestrating hybrid human-agent ecosystems.

---

## 5. Data Readiness for the Agentic AI Era

The Gartner research surfaced by the NICE CX trends checklist makes a critical point: fragmented or unreliable data is the silent barrier to scaling AI. When data isn't trusted or connected, AI decisions slow down, customer journeys fragment, and ROI suffers.

A Gartner survey found that only about a third of organisations running AI initiatives have a systematic data readiness process. The remaining majority are doing it ad hoc, which becomes especially concerning once you factor in agentic AI, where agents operate autonomously and need context to function properly. Without AI-ready data, an agent struggles to identify whether it's being prompted in the right context for the right use case.

Gartner recommends five steps for data and analytics leaders on the journey to AI readiness: assess data management readiness, gain executive buy-in, evolve data management practices, extend the data ecosystem, and scale with governance. What's notable is how well this maps onto the work PCMH is already doing:

- Our **FHIR-native architecture on WIS** gives us structured, standards-based data.
- The **Oracle-to-PostgreSQL migration** gives us open, portable infrastructure.
- The **cloud migration** gives us scalable compute.
- Our **Ardoq capability mapping** gives us the metadata layer that helps answer the question: "is our data AI-ready?"

!!! warning "The cautionary stat"
    Gartner predicts that by 2028, 40% of agentic AI projects will be cancelled due to escalating costs, unclear business value, or inadequate risk controls. The organisations that succeed will be those that pair rapid innovation with disciplined data control, infrastructure readiness, and responsible governance. That is exactly the balance we're trying to strike.

---

## 6. Observability and Production: Where the Rigor Goes

As we shift to AI-assisted development and prepare for cloud migration later this year, we need to put quality at the heart of what we do even more than we do right now. Not just testing quality, not just code review quality, but the quality of our understanding of what our systems are actually doing in the hands of real users. That means observability.

Charity Majors published a piece in March 2026 that crystallises something our industry has been getting wrong for decades, and that we cannot afford to carry forward into the AI era. Her argument, responding to the Thoughtworks/Martin Fowler summit on AI-native software engineering, is that the most respected minds in our field are still relegating production to the realm of bugs and incidents. That's a blind spot we need to close.

**The core argument:** When the summit asked "where does the rigor go?" as AI takes over code generation, they identified five destinations: specification review, test suites, type systems, risk mapping, and continuous comprehension. All good. But production didn't make the list. If control is supposed to move "closer to reality," then production is as close to reality as you can get. Production is reality.

**The reframe:** Observability is a tool for understanding, not just for finding bugs. Formal methods and test suites are flight simulators. Production is flying the actual plane. Observability is how you fly it.

As we move to Cloud, and introduce AI-assisted development patterns that will increase our rate of change, these things demand that we think differently about how we understand our systems in production.

Right now, Azure Application Insights gives us basic telemetry. That's not going to be enough. Application Insights is an infrastructure monitoring tool built for operators. What we need is something that lets builders ask precise, exploratory questions about user behaviour, product quality, and areas of improvement. Dashboards show you what you already decided to measure. Observability lets you ask questions you didn't know you needed to ask.

**The shift-everywhere question:** We talk about shift-left (catching problems earlier in development) and shift-right (testing in production). Majors' argument is that this framing still treats production as secondary. What we need is to shift everywhere: rich, contextual telemetry that becomes a continuous feedback loop from the moment code is written through to its behaviour under real-world conditions.

**What "shift everywhere" looks like for us:** Instrument as you go, not after the fact. Ship and validate your change in production. See what users actually do with it. Ship another change based on what you learn. Connect developer intent with outcomes in production through short, fast feedback loops. This is not new thinking; it predates both AI and DevOps. But AI makes it non-optional, because when the rate of change increases tenfold, all the duct tape comes off.

### AI Breaks the "Good Enough" Economy

Majors identifies two reasons why most teams haven't built proper production feedback loops: the ecosystem of tooling needed (feature flags, progressive deployments, granular observability) has been out of reach, and the old ways were good enough. Systems evolved to tolerate a certain rate of change, held together by human intuition, long-tenured engineers, and duct tape.

AI breaks both of those. It brings the cost of instrumentation down dramatically at the same time as it turns the evolutionary rate of change into a bottleneck and existential risk. When code is being generated at agentic speed, you have to validate at agentic speed. You have to encode context into your systems instead of relying on human intuition to bridge the gaps.

The pharma industry learned this the hard way. They used to treat evaluation as a checkpoint: test before you ship, pass the gate, you're in production. Catastrophic failures forced them to develop continuous monitoring of conditions over time. As AI-generated code becomes the norm, software engineering faces the same reckoning. The spec describes intent. Telemetry describes reality. Or as one practitioner put it: *production telemetry is the spec that survived.*

!!! note "The unwritten chapter"
    This part of our playbook is unwritten. We know we need richer observability than Application Insights provides. We know our cloud migration is the natural moment to get this right. We know that the Agentic QE model (Section 4) and the data readiness work (Section 5) both depend on production telemetry as a feedback mechanism. But we haven't yet defined what our observability stack looks like, what we instrument, or how we build the feedback loops that connect developer intent to production outcomes.

### Observability & Production Resources

**[Production Is Where the Rigor Goes](https://charity.wtf)** *(Charity Majors, March 2026)*
The article that frames this entire section. Essential reading for everyone in the group. Responds to the Thoughtworks AI-native summit and argues that production must be at the centre of where rigor relocates to.

**Relocating Rigor** *(Chad Fowler)*
The essay that prompted the summit's central question. Argues that when code generation gets easier, judgment must get stricter. Constraint removal relocates rigour rather than removing it.

**The Software Development Lifecycle is Dead** *(Boris Tane)*
A provocative companion piece. Argues that when agents ship code faster than humans can review it, the observability layer becomes the primary safety mechanism and the connective tissue of the whole system.

**The Eval Crisis: Why Testing AI Like Software Is Failing Us** *(Yasmeen Ahmad)*
Argues we're applying a testing approach to what is essentially an epidemiological problem. When controlled testing can't capture what matters, you instrument the deployed system and measure outcomes, not just outputs.

**Finding Comfort in the Uncertainty** *(Annie Vella)*
Reflections from the Thoughtworks summit. The key takeaway: nobody has this figured out. Honest, grounded, and a good counterweight to the hype.

**The Future of Software Development** *(Thoughtworks Summit Readout)*
The full summit summary that prompted Majors' response. Ten thematic buckets covering how software engineering is changing in the AI-native era. Worth reading alongside the critique.

**[Observability Engineering](https://www.honeycomb.io/books/observability-engineering/)** *(O'Reilly, free ebook)*
The definitive guide to observability as a discipline. Free from Honeycomb. If you read one book on this topic, make it this one.

**[OpenTelemetry](https://opentelemetry.io)**
The open-source, vendor-neutral standard for instrumentation. Whatever observability stack we choose, OpenTelemetry is the instrumentation layer. Worth understanding now.

---

## 7. Branching Strategies, Continuous Integration, and Working Agreements

As we move our repositories to GitHub and introduce AI-assisted development, we need to get our branching strategy right. This isn't a peripheral concern. The branching model a team uses determines whether continuous integration is possible, and without continuous integration, there is no continuous delivery. Everything else in this playbook depends on it. DHCW's second strategic principle is simplifying everything we do. Trunk-based development is what simplification looks like in version control: fewer branches, fewer merges, fewer surprises, and faster feedback.

The [Beyond MinimumCD Practice Guide](https://bdfinst.github.io/beyond-minimumcd/), maintained by Bryan Finster and the Dojo Consortium, is the definitive resource here. It's grounded in [MinimumCD.org](https://minimumcd.org) and provides practices, patterns, and concrete solutions for every team migrating to continuous delivery. The central question it asks is simple and uncomfortable: *"Why can't you ship today's work today?"*

### Trunk-Based Development: The Branching Model for CD

MinimumCD is clear: trunk-based development is the branching pattern required to meet the definition of continuous integration. Not GitFlow. Not long-lived feature branches. Not release branches with extensive backporting. Trunk-based development. The reasons are well documented: long-lived branches guarantee merge conflicts, prevent fast feedback, accumulate risk silently, and turn merging into a project in itself.

**What trunk-based means in practice:**

- Every developer integrates to trunk at least once per day.
- Branches, if used, live for less than 24 hours.
- No long-lived feature, development, or release branches.
- Changes are small enough for genuine review. A 50-line change gets careful attention; a 3,000-line merge request gets skimmed.
- The team maintains a shared understanding of how the codebase is evolving because they see every change as it happens.

The common objection in regulated environments like ours is that trunk-based development is incompatible with compliance. The Beyond MinimumCD guide addresses this directly: TBD is about integration frequency, not about eliminating controls. Every change can still be traceable to a requirement, attributable to a specific individual, reviewed before reaching production, and subject to a documented approval workflow. Short-lived branches with daily integration satisfy all of these requirements while maintaining the benefits of continuous integration.

### Working Agreements: Making the Commitment Explicit

The [Beyond MinimumCD Working Agreements page](https://bdfinst.github.io/beyond-minimumcd/working-agreements) is essential reading for every delivery team in PCMH. CD practices only work when the whole team commits to them, and working agreements make that commitment explicit. Without them, practices drift: one developer integrates daily while another keeps a branch for a week. These inconsistencies compound quickly.

The guide defines three foundational agreements that every team needs:

**Definition of Done:** A work item is done when code is integrated to trunk, all automated tests pass, code has been reviewed, the change is delivered to the end user (or deployable to production at any time), no known defects are introduced, and feature flags are in place for incomplete user-facing features. The critical phrase is "delivered to the end user." Many teams define done as "code is merged." That creates a gap between done and delivered where risk accumulates silently.

**Definition of Ready:** A work item is ready when acceptance criteria are defined and specific, the item is small enough to complete in two days or less, it is testable, dependencies are identified, and the team has discussed it. The two-day ceiling is important: it forces decomposition into small, integrable increments. This is the discipline that makes trunk-based development possible.

**CI Working Agreement:** Every developer integrates to trunk at least daily. Branches live for less than 24 hours. All tests must pass before merging. A broken build is the team's top priority: it gets fixed before any new work begins. If the fix takes more than 10–15 minutes, revert the change and fix it offline. No one commits to a broken trunk except to fix the break.

### Stop the Line: Why This Matters for Clinical Systems

The "broken build = top priority" agreement is the single most important CI discipline. The guide illustrates this with two timelines: a team that stops all feature work when the build breaks typically restores green in 20–30 minutes. A team that treats it as one person's problem while others keep committing typically loses half a day or more to compounding conflicts. The team that stops immediately pays a small, predictable cost. The team that doesn't pays a large, unpredictable one.

The stop-the-line discipline isn't heavy-handed. It's the team protecting its own ability to deliver safely.

AI-assisted development makes this more urgent, not less. When code is being generated at agentic speed, the rate of integration increases. That means the feedback loops need to be tighter, the branches need to be shorter, and the working agreements need to be explicit. The Beyond MinimumCD guide includes an entire section on Agentic CD covering constraints and practices for AI agent-generated changes, including repository readiness, prompting disciplines, agent delivery contracts, and pipeline enforcement for agent-generated code.

**The anti-patterns to watch for:** The guide catalogues branching and integration anti-patterns that directly apply to our context: long-lived feature branches, deferred integration, cherry-pick releases, release branches with extensive backporting. It also covers organisational anti-patterns we should be honest about: Change Advisory Board gates, hardening sprints, deployment windows, and siloed QA teams. These are all things that exist in our current operating model. This guide gives us the language and evidence to evolve them.

### Branching, CI & Working Agreements Resources

**[Beyond MinimumCD Practice Guide](https://bdfinst.github.io/beyond-minimumcd/)**
The comprehensive guide. Start with the migration path: Assess → Foundations → Pipeline → Optimise → Deliver on Demand. Includes a symptom triage tool, anti-pattern catalogue, and pipeline reference architecture.

**[Working Agreements](https://bdfinst.github.io/beyond-minimumcd/working-agreements)** *(Beyond MinimumCD)*
The page that frames this section. Covers Definition of Done, Definition of Ready, and the CI Working Agreement with templates and measurement criteria. Essential reading for every delivery team.

**[TBD Migration Guide](https://bdfinst.github.io/beyond-minimumcd/tbd-migration)** *(Beyond MinimumCD)*
Tactical guide for migrating from GitFlow or long-lived branches to trunk-based development. Covers regulated environments, multi-team coordination, compliance misconceptions, and common pitfalls. Directly relevant to our GitHub migration.

**[Long-Lived Feature Branches Anti-Pattern](https://bdfinst.github.io/beyond-minimumcd/long-lived-branches)** *(Beyond MinimumCD)*
Why branches that live for weeks or months turn merging into a project. Includes retrospective questions for teams to self-assess, and the path to daily integration.

**[Agentic CD](https://bdfinst.github.io/beyond-minimumcd/agentic-cd)** *(Beyond MinimumCD)*
Constraints and practices for AI agent-generated changes. Covers getting started, repository readiness, prompting disciplines, agent delivery contracts, pipeline enforcement, and tokenomics. This is where the branching strategy meets our AI-assisted development approach.

**[MinimumCD.org](https://minimumcd.org)**
The original manifesto. The minimum definition of continuous delivery, signed by practitioners across the industry. Short, sharp, and worth reading before anything else on this list.

**[trunkbaseddevelopment.com](https://trunkbaseddevelopment.com)**
Paul Hammant's comprehensive reference site for trunk-based development. Covers every variant, every objection, and every edge case. The definitive technical reference.

**[Strangler Fig Application](https://martinfowler.com/bliki/StranglerFigApplication.html)** *(Martin Fowler)*
Explains how to incrementally replace a legacy system by building new functionality around it, routing traffic to the new system over time.

**[Blazor .NET](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor)**
Our target web framework. Chosen because the team has C# expertise, and Blazor allows us to build interactive web UIs with the language we already know.

**[GOV.UK Notify](https://www.notifications.service.gov.uk)**
Integration opportunity identified for patient and parent communications in service modernisation work.

---

## 9. Foundational Reading and Thinking

Everything we're doing sits on a foundation of established thinking about delivery, architecture, and engineering culture. These aren't new resources, but they're the bedrock.

### Delivery & Quality

**[Bryan Finster: Quality Principles](https://bdfinst.github.io)**
Quality is user-defined. Deliver small and frequently. "You build it, you run it." QA/SDET enables better developer testing rather than gatekeeping. These principles already shape how we work; AI just gives us better tools to live them.

**[DORA Research Programme](https://dora.dev)**
The research base for everything we measure. Deployment frequency, lead time for changes, change failure rate, time to restore service. Our PRISM dashboard is built around these metrics.

**[Charity Majors](https://charity.wtf)** *(charity.wtf)*
Observability, engineering culture, and AI in production. Her writing on observability 2.0 directly informs our thinking about product dashboards and continuous governance.

### Architecture & Systems Thinking

**[Fundamentals of Software Architecture](https://www.oreilly.com/library/view/fundamentals-of-software/9781492043447/)** *(Richards & Ford)*
The best on-ramp to systems-level thinking. Essential reading for anyone working on service modernisation or WIS architectural decisions.

**[Designing Data-Intensive Applications](https://www.oreilly.com/library/view/designing-data-intensive-applications/9781491903063/)** *(Martin Kleppmann)*
Dense but transformative. Directly applicable to our FHIR data flows, our database migration work, and our thinking about data readiness.

**[Building Microservices](https://www.oreilly.com/library/view/building-microservices-2nd/9781492034018/)** *(Sam Newman)*
Directly applicable to WIS's microservices architecture. A practical guide to the patterns we're already using and the ones we're evolving towards.

### Channels to Follow

**[GOTO Conferences](https://www.youtube.com/@GOTO-)** *(YouTube)*
Real practitioners on real decisions. The best conference talk channel for senior engineers and delivery leads.

**[ByteByteGo](https://www.youtube.com/@ByteByteGo)** *(YouTube)*
Clear system design explainers. Useful for visual learners and anyone wanting to understand distributed systems patterns.

**[Fireship](https://www.youtube.com/@Fireship)** *(YouTube)*
Sharp, fast overviews of emerging tools and frameworks. Good for staying current without a massive time commitment.

**Podcasts:** Software Engineering Daily &bull; Changelog &bull; Chain of Thought (Galileo AI)
For deeper dives on agentic systems, continuous delivery, and engineering culture.

---

*We're figuring this out together. Be curious. Be kind. Build things that matter.*

*Peidiwch ag aros. Don't wait.* 🏴󠁧󠁢󠁷󠁬󠁳󠁿
