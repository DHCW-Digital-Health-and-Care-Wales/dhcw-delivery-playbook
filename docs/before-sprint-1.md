# Before Sprint 1: setting up to succeed

## Team charter

Before writing code, a product team must align on how they work together. High-performing teams build a social framework deliberately. A Team Charter is a short, co-created document that binds cultural expectations with day-to-day working agreements. It is created by the whole team during **Sprint 0**.

### Identity and structure

As a team, create your own identity within the framework that DHCW provides. Agree a team name (this can be something fun). List who is accountable for what. Map skills across the team so everyone knows who to go to for help. Where a role is missing or shared, the team must agree explicitly who carries each responsibility. Gaps in accountability create delivery risk.

### Team vision

A short statement that explains why the team exists and what value it provides. This should link back to DHCW's vision to "Make Digital a Force for Good in Health and Care". Everyone in the team should be able to say it. A good vision names the user and the outcome:

!!! example "Example – Vaccinations"
    To provide one national digital service, from stock to surveillance. Finding, protecting, remembering, and learning, so that vaccination in Wales stays prudent, equitable, and evidence-led.

### Core values

The behavioural commitments the team makes to each other. There is an overlap between our DHCW values, compassionate leadership principles, and agile working values. These underpin psychological safety and good conflict resolution. Common examples from DHCW teams include:

- **Transparency** – we share work in progress, problems, and mistakes early
- **Collaboration** – we solve problems together rather than in isolation
- **Respect** – we value each other's contribution regardless of seniority
- **Honesty** – we give and receive feedback as a normal part of working

### Working agreements

Specific, measurable commitments about how the team communicates and coordinates day to day. The team sets these. Examples:

- Core collaboration hours: the hours between 9am and 5pm when everyone is available for ceremonies, pairing, and questions
- Avoid direct messages: share thinking, questions, and uncertainty in the open and make everyone feel included. Use the team channel for discussions, as direct messages can become hidden decision threads
- Respond to messages within two working hours during collaboration hours
- Pull request reviews completed within four hours of posting. Post the PR link in the team channel
- Update Azure DevOps tickets daily. If it isn't in ADO, it doesn't exist
- Notify the team of planned leave at least four weeks in advance

### Success metrics

Agree how the team will know it's working well, beyond hitting sprint targets. Combine quantitative measures (deployment frequency, cycle time, defect rates) with qualitative ones (team morale, retrospective quality). DORA metrics (Deployment Frequency, Lead Time for Change, Time to Restore Service, and Change Failure Rate) are the primary engineering health measures at DHCW.

## Tooling

DHCW teams use a consistent tooling stack to support collaboration and delivery.

| Tool | Purpose |
| --- | --- |
| **Azure DevOps** | Source of truth for all work tracking. Every ticket, sprint, and delivery plan lives here. If it's not in ADO, it doesn't exist. |
| **GitHub** | Source code, version control, pull requests, and CI/CD pipelines. DHCW teams are migrating to GitHub as the primary code platform. GitHub Copilot is available for teams that are ready to use it, in line with the AI Engineering Strategy. |
| **Miro** | Virtual whiteboard for retrospectives, journey mapping, architecture sketching, and workshops. Teams use Miro for collaborative sessions; working decisions should be captured in ADO or written documentation. |
| **Figma** | DHCW uses a dual design system approach that connects Figma-based design with coded components, keeping UCD and engineering working from the same foundation. Designers can prototype and iterate rapidly without writing code, test concepts with users at low cost, and improve in real time based on feedback. Engineers use the Figma library as a visual reference for design intent, reducing ambiguity when building. |
| **Component Library (GitHub)** | The coded component library available through GitHub. Prototypes built in code are more realistic, which produces better usability testing results and sharper design decisions. Reusable coded components mean engineers spend less time writing UI code and more time on the parts of the product that require bespoke work. Because prototypes and final builds share the same components, the gap between what was tested and what gets shipped is much smaller. Together with Figma, the two layers reduce rework, increase visibility of what already exists across the portfolio, and give both UCD and engineering teams a shared resource to build from. |

## Sprint 0: launching a new team

Sprint 0 is the setup phase before delivery begins. It runs for two to three weeks and establishes the conditions for sustained, high-quality delivery. It is when the team forms as a team.

### Week 1 – infrastructure and alignment

- Delivery manager, product owner, and lead software engineer configure Azure DevOps, link to GitHub, provision environments, and set up Miro
- Grant team access to all tools and confirm Welsh Language and accessibility commitments are understood
- Hold an in-person kick-off workshop. Run the Team Charter workshop. Agree a draft Definition of Ready and Definition of Done
- Confirm alignment to the Digital Service Standard for Wales using the [service standard self-assessment](https://nhswales365.sharepoint.com/sites/DHC_UCD/SitePages/Service-standard-self-assessment.aspx) (NHS Wales sign-in required), and identify which phase the product is in

### Week 2 – planning and backlog setup

- Product owner leads a high-level product mapping session in Miro, establishing the now / next / later roadmap
- Collaboratively break down high-level goals into epics and features in ADO
- Begin backlog refinement: break features into user stories with the whole team
- Complete a baseline estimation exercise so the team shares a common understanding of relative size

### Week 3 – first sprint

- Delivery manager sends calendar invites for all sprint ceremonies
- First Sprint Planning: agree the sprint goal and pull a sprint backlog. Sprint 1 is typically heavier on spikes as the team learns the codebase and system
- Activate the ADO sprint board and the GitHub repository

!!! info "Welsh language in Sprint 0"
    Every team must confirm Welsh Language requirements before Sprint 1 begins. This means understanding which elements of the service are user-facing, agreeing how Welsh content will be created and maintained, and ensuring the Definition of Done includes a Welsh Language check for user-facing changes.
