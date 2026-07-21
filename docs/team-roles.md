# Team roles

DHCW uses the Government Digital and Data (GDaD, formerly DDaT) capability framework for all professional roles in product and service delivery. We describe a product team as a small, stable **core** with a set of **attached capabilities** that join for a period and change over time. The point is not who reports to whom. The point is that everyone working with the team, for as long as they are working with it, is a member of the team.

The **core** is the part of the team that stays constant across the whole service lifecycle. The Product Owner and Delivery Manager are core members present at every phase, alongside the engineering and test capability that builds and assures the product. The core carries the memory of the work: the decisions made, the user needs uncovered, and the reasons behind them.

**Attached capabilities** are roles that join the team for a period and then move on as the need changes. User-centred design (UCD) roles, the Business Analyst, and architecture roles are all attached capabilities. Their involvement is normally heaviest during discovery and alpha, when the team is shaping the problem and testing an approach, and lighter in beta and live. Architecture is treated exactly like the UCD roles: an attached capability that joins the team, not an external function that reviews it from outside.

The cultural message matters more than the diagram. If you are allocated to a team for a sprint, you are on that team for that sprint. You attend its ceremonies, you share its goals, and you take shared responsibility for what it ships. Attached does not mean part-time in commitment. It means part-time in duration.

``` mermaid
graph TD
    subgraph Core [Core: present at every phase]
        PO[Product Owner]
        DM[Delivery Manager]
        ENG[Engineering capability]
        TEST[Test capability]
    end
    subgraph Attached [Attached capabilities: join for a period]
        UCD[UCD roles]
        BA[Business Analyst]
        ARCH[Architecture roles]
    end
    UCD --> Core
    BA --> Core
    ARCH --> Core
```

The diagram shows the point of the model: architecture sits inside the ring of attached capabilities alongside UCD and business analysis, joining the team rather than reviewing it from outside.

## The core team

A product team has no traditional management hierarchy. The Product Owner and Delivery Manager have a joint, collaborative relationship at the heart of the team, but they are not directing it from above. The Product Owner is focused on the problem space: what the team is building, for whom, and why. The Delivery Manager is focused on the team itself: creating the conditions for good work, removing blockers, handling the practical realities of line management, and making sure the team has what it needs to sustain a healthy pace. Neither role tells the team what to do. Both roles serve it.

Teams are expected to be self-organising. The people closest to the work make the decisions about how to do it. The Service Owner sets the direction and holds accountability for outcomes, but within that boundary the team has genuine autonomy. That autonomy only works if the team takes it seriously: self-organisation is the deliberate choice to build structure together rather than have it imposed.

| GDaD role | DHCW band | Purpose |
| --- | --- | --- |
| **Product Owner** | Band 6–8A | Maximises the value of the product. Owns the backlog, defines priorities, and represents user and business needs to the team. The Product Owner is the decision-maker on what gets built and in what order, and is a core member present at every phase. |
| **Delivery Manager** | Band 6–8A | Optimises team delivery, removes blockers, and coaches the team in agile practices. Facilitates ceremonies and protects the team from external interruptions. The Delivery Manager serves the team, not the other way around, and is a core member present at every phase. |
| **Senior Software Engineer** | Band 7 | Owns the technical vision and architectural integrity of the product. Mentors the engineering team, evaluates feasibility, and works closely with the Product Owner to ensure technical investment is prioritised alongside feature delivery. |
| **Software Engineer** | Band 4–6 | Designs, builds, and maintains production-grade code. Writes tests, reviews colleagues' code, and takes shared responsibility for the quality of what the team ships. Engineers at DHCW are expected to contribute to the full delivery lifecycle, not only to coding tasks. |
| **Test Engineer** | Band 4–7 | Quality is a whole-team responsibility, not a separate gate. Test Engineers bring specialist skills in test strategy, automation, and exploratory testing. They help the team build quality in from the start, rather than inspect it at the end. |

!!! info "A note on team size and composition"
    DHCW product teams typically include 4 software engineers and 2 test engineers per team, supported by a Product Owner and Delivery Manager as the stable core. Attached capabilities may be shared across teams or brought in for specific pieces of work. Where roles are shared, the team must agree clearly on how time is split and who owns each responsibility.

## Attached capabilities

Attached capabilities join the team for a period, contribute as full members while they are allocated, and move on when the need changes. Their involvement is normally heaviest during discovery and alpha and lighter in beta and live, but the pattern varies by service. Architecture roles are listed here alongside the UCD roles because they work the same way: they join the team, take part in its ceremonies, and share its goals for as long as they are allocated to it.

| GDaD role | DHCW band | Purpose |
| --- | --- | --- |
| **Interaction Designer** | Band 6–8A | Works out the best way to let users interact with services, in terms of both overall flow and individual design elements. Works with Product Owners and Engineers to ensure components and interactions are well designed and achievable. |
| **Service Designer** | Band 7–8A | Designs the end-to-end journey of a service, making sure it meets user needs across every touchpoint, channel, and team boundary. Works with Product Owners, Delivery Managers, clinical stakeholders, and members of the public to map how people experience a service in full, not just the digital parts, and to identify where design changes will have the most impact on outcomes. |
| **Content Designer** | Band 6–8A | Makes sure the right information reaches the right people in the right way. Works with user researchers and interaction designers to understand what users need to know, then designs content that is clear, accessible, and written in plain language. At DHCW, this includes ensuring all user-facing content meets Welsh Language Standards and works equally well in both languages from the outset. |
| **Business Analyst** | Band 6–7 | Bridges product-level requirements and technical execution. Collaborates with the whole team to develop user stories, acceptance criteria, and process flows. Supports refinement, but story creation is a team activity, not a BA handoff. |
| **Solution Architect** | Band 7 and above | Shapes the technical approach for a specific service, balancing user need, feasibility, and fit with existing systems. Joins the team to make and record significant design decisions, particularly during discovery and alpha. |
| **Technical Architect** | Band 7 and above | Guides detailed technical design and the choice of technologies, patterns, and standards. Works with the engineering capability at points of significant design decision and where work touches shared platforms. |
| **Enterprise Architect** | Band 8A and above | Aligns individual services with the wider technology landscape, national infrastructure, and interoperability standards. Engages when a team is making choices that affect, or are affected by, systems beyond its own service. |

!!! info "Allocation is membership"
    At DHCW, architectural oversight is coordinated through the Technical Design and Assurance function, and teams should involve their allocated architect early, before committing to major technical direction. While an architect is allocated to a team, they are a member of that team: they attend the ceremonies that are relevant to their work and share responsibility for the outcome, in the same way as any other attached capability.

## The Service Owner

Above the product team sits the Service Owner (typically Band 8B), who is accountable for how well the service meets user needs. The Service Owner is not a day-to-day team member but sets direction, represents the service to stakeholders and governance bodies, and holds accountability for outcomes. The Product Owner works within the direction set by the Service Owner.

## Capabilities across the lifecycle

The table below shows how the core and attached capabilities engage across the service lifecycle. The Product Owner and Delivery Manager are core in every phase. Engineering and test are also core, growing from a lighter presence in discovery to full delivery in beta and live. Attached capabilities are heaviest during discovery and alpha and lighter later, but they remain full members of the team whenever they are allocated to it.

| Capability | Discovery | Alpha | Beta | Live |
| --- | --- | --- | --- | --- |
| Product Owner | Core | Core | Core | Core |
| Delivery Manager | Core | Core | Core | Core |
| Engineering | Core | Core | Core | Core |
| Test | Core | Core | Core | Core |
| UCD roles | Attached, heaviest | Attached, heaviest | Attached | Attached, lighter |
| Business Analyst | Attached, heaviest | Attached | Attached | Attached, lighter |
| Architecture roles | Attached, heaviest | Attached, heaviest | Attached | Attached, lighter |
