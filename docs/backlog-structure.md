# Backlog structure

## Ticket hierarchy

Everything the team does is tracked in Azure DevOps. The ticket hierarchy below applies across all DHCW product teams.

| Level | Type | Description | Horizon | Owner |
| --- | --- | --- | --- | --- |
| 1 | **Epic** | A substantial strategic initiative or major investment area. | 1 month+ | Product Owner |
| 2 | **Feature** | A distinct, functional component of an Epic. Delivers meaningful value when complete. | 1–6 sprints | Product Owner |
| 3 | **User Story** | Describes what needs to be built to unlock user value. Written from the user's perspective. | Within sprint | Product team |
| 3 | **Bug** | Incorrect or broken behaviour in the system that needs fixing. | Within sprint | Product team |
| 3 | **Spike** | Research or investigation to reduce uncertainty before building. Must have a clear outcome and be time-boxed. | Within sprint | Product team |
| 3 | **Task** | Work that does not deliver a direct user-facing feature: training, continuous improvement, documentation, or technical maintenance. | Within sprint | Product team |
| 4 | **Sub-task (optional)** | Breakdown of steps within a user story. Use sparingly: if a story needs more than three sub-tasks, it is probably too large. | Within sprint | Engineers |

## Tagging user stories and epics

Every Epic and User Story carries one organisation-level tag. Tags give DHCW a consistent view across teams of where effort is going, so leadership can see the balance between new value, maintenance, and learning across the whole portfolio. Tags are applied in Azure DevOps and add a portfolio view on top of the work item type.

| Tag | When to use it |
| --- | --- |
| **New Feature** | Work that delivers new user-facing value or a new capability. |
| **Tech Debt** | Work that improves the health of the codebase, platform, or tooling without adding new user-facing value. See the Technical debt page for guidance on identifying and prioritising it. |
| **Bug** | Work to correct incorrect or broken behaviour in the system. |
| **Research and Development** | Work to reduce uncertainty or explore a new idea, such as a spike or a proof of concept. |

!!! info "Bug is both a work item type and a tag"
    Bug appears in the ticket hierarchy as a work item type and here as an organisation-level tag. Every ticket raised as a Bug work item type is tagged Bug. The tag also lets us report on corrective work that is captured inside a User Story rather than as a standalone Bug ticket.

## Definition of Ready

A ticket is ready for sprint planning when it meets all of the following criteria. If it fails any of these, it stays in the backlog for further refinement. The team has the right to reject tickets at refinement.

The team should always look to have a runway of two to three sprints worth of work that is "ready" to be taken into sprint. This ensures a steady pipeline of work, realistic near-term planning, and allows the team to respond to unexpected events.

- [ ] User story or ticket is written in a format the team understands
- [ ] Acceptance criteria are defined and testable (Given / When / Then format recommended)
- [ ] The ticket is small enough to complete within a single sprint
- [ ] Dependencies are identified and noted on the ticket
- [ ] The technical platform the story is built on is ready before the story enters the sprint
- [ ] Designs or wireframes are attached where the ticket has a user-facing interface
- [ ] Welsh Language requirements for any user-facing content have been considered
- [ ] The team has reviewed the ticket at refinement and estimates it collectively

!!! info "What platform ready means"
    A story is only ready when the technical platform it depends on already exists. The environments, services, pipelines, and infrastructure the story needs must be in place and usable before the story enters the sprint. If the platform is still being built, that platform work is a dependency in its own right and must be completed first. Pulling a story into a sprint before its platform is ready leads to blocked work and unreliable delivery forecasts.

## Definition of Done

A ticket is done when it meets all of the following criteria. These standards apply uniformly across all ticket types unless the team has agreed a specific exception and documented it. Quality is the whole team's responsibility: there is no separate QA gate.

- [ ] Code is reviewed and approved by at least one peer and merged to the main branch. Pairing or mobbing on the change counts, since the review happens as the work is done
- [ ] All automated tests pass in the CI/CD pipeline
- [ ] Unit tests cover all new functionality and pass
- [ ] Integration tests are written and pass
- [ ] API automated tests cover at least 80% of the story's acceptance criteria
- [ ] Acceptance criteria are met and have been validated against the running software
- [ ] No known defects have been introduced
- [ ] Technical and user-facing documentation is updated where needed
- [ ] The change is production-ready and deployable to production at any time, behind a feature flag where needed
- [ ] Azure DevOps ticket is updated and closed
- [ ] Release notes or change log updated
- [ ] The appropriate local engineering process has been followed

!!! info "Continuous delivery is the expectation"
    A change that meets this Definition of Done is production-ready and can deploy to production at any time. Teams that don't yet deploy straight to production use a staging or QA environment as an interim step, and are expected to keep moving towards continuous delivery over time.

The team reviews its Definition of Done at each retrospective to keep it relevant and current.

### Cross-cutting controls

Cross-cutting controls are legal, safety, or organisational requirements that apply to every ticket regardless of type. Unlike the criteria above, these cannot be waived by a team-level exception: they reflect obligations placed on DHCW as an organisation. Where a control does not apply to a given ticket, record why on the ticket rather than removing the check.

- [ ] Cyber security requirements for the change have been met, including secure handling of any data the change touches
- [ ] User-facing interfaces meet WCAG 2.2 AA accessibility standards
- [ ] User-facing content meets Welsh Language Standards
- [ ] The change meets applicable technical and data standards
- [ ] Clinical safety obligations have been met where the change is in scope (DCB0129 / DCB0160)

## Product Goal

A backlog tells you what you might build. A Product Goal tells you where you are heading, and why. It is the one meaningful outcome the team is working towards right now, written plainly enough that everyone can repeat it.

A good Product Goal describes a future state of the product that matters to users. "Every eligible child in Wales has an accurate, near real-time immunisation record" is a Product Goal. It is bigger than a single sprint and smaller than the whole roadmap. It sits at the top of the backlog, and the rest of the backlog exists to reach it. Every sprint goal should point at it.

Work towards one Product Goal at a time. Reach it, or decide together to let it go, before you take on the next. Holding a single goal keeps the team pulling in one direction, and it makes it obvious when a piece of work has drifted away from what matters.

The Product Owner owns the Product Goal, shapes it with the team, and keeps it visible. Revisit it when the world changes. If it no longer describes where you are heading, change it in the open and tell people why.

## Product roadmap: Now, Next, Later

DHCW teams use a three-horizon roadmap to balance near-term delivery with longer-term direction. This framework keeps planning light while giving stakeholders a reasonable view of the direction of the product.

| Horizon | Timeframe | What it contains |
| --- | --- | --- |
| **Now** | 0–3 months | Refined user stories that meet the Definition of Ready. This is the firm near-term delivery commitment. |
| **Next** | 3–12 months | Features and epics in discovery or early refinement. Requirements are taking shape but not yet sprint-ready. T-shirt sizing is appropriate here. |
| **Later** | 12+ months | Strategic goals and product ideas. These are highly flexible and will shift as we learn more. They should not be over-specified. |

## Estimation

### T-shirt sizing

For roadmap planning and features in the Next and Later horizons, teams use t-shirt sizing to give a rough sense of scale. T-shirt sizing is a conversation starter.

| Size | Approximate scale |
| --- | --- |
| **XS** | Under 1 sprint |
| **S** | 1–2 sprints |
| **M** | 3–4 sprints |
| **L** | 5–6 sprints |
| **XL** | More than a quarter. If a feature reaches XL, consider whether it should be an epic. |

### Relative estimation

For sprint-level stories, teams estimate relative effort using a shared scale. The most common approach is the Fibonacci sequence (1, 2, 3, 5, 8, 13, 21), where the team agrees what a '1' and a '3' look like as reference points, then estimates everything else relative to those. The goal is a shared understanding of complexity.

!!! info "Estimation is a team conversation"
    Story points and t-shirt sizes are planning aids and a valuable way of capturing discussion and shared understanding of the complexity of work. If your team is debating whether something is a 5 or an 8, the debate itself is the value.
