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

## Definition of Ready

A ticket is ready for sprint planning when it meets all of the following criteria. If it fails any of these, it stays in the backlog for further refinement. The team has the right to reject tickets at refinement.

The team should always look to have a runway of two to three sprints worth of work that is "ready" to be taken into sprint. This ensures a steady pipeline of work, realistic near-term planning, and allows the team to respond to unexpected events.

- [ ] User story or ticket is written in a format the team understands
- [ ] Acceptance criteria are defined and testable (Given / When / Then format recommended)
- [ ] The ticket is small enough to complete within a single sprint
- [ ] Dependencies are identified and noted on the ticket
- [ ] Designs or wireframes are attached where the ticket has a user-facing interface
- [ ] Welsh Language requirements for any user-facing content have been considered
- [ ] The team has reviewed the ticket at refinement and estimates it collectively

## Definition of Done

A ticket is done when it meets all of the following criteria. These standards apply uniformly across all ticket types unless the team has agreed a specific exception and documented it. Quality is the whole team's responsibility: there is no separate QA gate.

- [ ] Code is reviewed by at least one peer and merged to the main branch
- [ ] All automated tests pass in the CI/CD pipeline
- [ ] New functionality is covered by automated tests at an appropriate level
- [ ] The change is deployable to production at any time (or protected behind a feature flag)
- [ ] Acceptance criteria are met and have been validated against the running software
- [ ] No known defects have been introduced
- [ ] User-facing content meets Welsh Language Standards
- [ ] User-facing interfaces meet WCAG 2.1 AA accessibility standards
- [ ] Azure DevOps ticket is updated and closed
- [ ] Release notes or change log updated

## Product roadmap: Now, Next, Later

DHCW teams use a three-horizon roadmap to balance near-term delivery with longer-term direction. This framework keeps planning light while giving stakeholders a reasonable view of the direction of the product.

| Horizon | Timeframe | What it contains |
| --- | --- | --- |
| **Now** | 0–3 months | Refined user stories that meet the Definition of Ready. This is the firm near-term delivery commitment. |
| **Next** | 3–12 months | Features and epics in discovery or early refinement. Requirements are taking shape but not yet sprint-ready. T-shirt sizing is appropriate here. |
| **Later** | 12+ months | Strategic goals and product ideas. These are highly flexible and will shift as we learn more. They should not be over-specified. |

## Estimation

### T-shirt sizing

For roadmap planning and features in the Next and Later horizons, teams use t-shirt sizing to give a rough sense of scale. T-shirt sizing is a conversation starter, not a commitment.

| Size | Approximate scale |
| --- | --- |
| **XS** | Under 1 sprint |
| **S** | 1–2 sprints |
| **M** | 3–4 sprints |
| **L** | 5–6 sprints |
| **XL** | More than a quarter. If a feature reaches XL, consider whether it should be an epic. |

### Relative estimation

For sprint-level stories, teams estimate relative effort using a shared scale. The most common approach is the Fibonacci sequence (1, 2, 3, 5, 8, 13, 21), where the team agrees what a '1' and a '3' look like as reference points, then estimates everything else relative to those. The goal is a shared understanding of complexity, not a prediction of hours.

!!! info "Estimation is a team conversation, not a number"
    Story points and t-shirt sizes are planning aids and a valuable way of capturing discussion and shared understanding of the complexity of work. If your team is debating whether something is a 5 or an 8, the debate itself is the value, not the number you land on.
