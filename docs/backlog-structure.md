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
