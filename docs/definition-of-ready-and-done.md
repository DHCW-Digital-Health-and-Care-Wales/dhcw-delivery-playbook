# Definition of Ready and Definition of Done

The Definition of Ready is the checklist a work item passes before the team picks it up. The Definition of Done is the checklist it passes before the team calls it finished. Both are defaults every DHCW team starts from. INVEST is a set of prompts for shaping user stories as they're refined, and the cross-cutting controls are obligations that apply to every work item and can't be waived.

## Definition of Ready

A work item is ready for sprint planning when it meets all of the following criteria. If it fails any of these, it stays in the backlog for further refinement. The team has the right to reject work items at refinement.

- [ ] The work item is written clearly, and the team understands it
- [ ] Acceptance criteria are defined and testable (Given / When / Then format recommended)
- [ ] The expected user or service outcome is stated on the work item, in terms specific enough to check whether it has been achieved
- [ ] Priority is set by the Product Owner
- [ ] Dependencies are identified and noted on the work item, and resolved where possible
- [ ] Designs or wireframes are attached where the work item has a user-facing interface
- [ ] Welsh Language requirements for any user-facing content have been considered
- [ ] The work item is small enough to complete within a single sprint
- [ ] The team has reviewed the work item at refinement and estimated it together

!!! note "Keep a runway of ready work"
    The team should always look to have a runway of two to three sprints worth of work that is "ready" to be taken into sprint. This ensures a steady pipeline of work, realistic near-term planning, and room to respond to unexpected events.

### INVEST criteria

INVEST is the lens the team uses to sense-check a user story as it's refined. The Definition of Ready and Definition of Done apply to every work item type; INVEST applies specifically to user stories. It's a quick heuristic, and some prompts here reinforce the checklist above, because the same quality shows up from more than one angle. Independent and Negotiable add the most beyond the checklist: they check whether the work can be finished without waiting on other work, and whether the designs and any API needs are understood.

**I – Independent**

- Checked against known cross-team and cross-programme dependencies
- Can be worked on and completed without relying on other stories
- Where dependencies exist, they are separated out and refined
- The team can complete the work without relying on other teams

**N – Negotiable**

- The story has been discussed and the team understands what needs to be done
- Interaction designs or wireframes exist, where appropriate, and the team understands them
- Interaction design stories are assessed for API requirements

**V – Valuable**

- The story states the value it delivers to users or stakeholders, in terms we can check once it is live
- Aligns with the product's goals
- Linked to its parent feature, so the value is traceable

**E – Estimable**

- Requirements and acceptance criteria are clear enough for the team to size the work together

**S – Small**

- The story is small enough to be completed within a single sprint

**T – Testable**

- The story can be tested to confirm the intended outcome or functionality has been achieved
- Acceptance criteria are well defined and specific enough to guide testing
- API stories conform to the local applicable standard or template

## Definition of Done

A work item is done when it meets all of the following criteria. These standards apply uniformly across all work item types unless the team has agreed a specific exception and documented it. Quality is the whole team's responsibility: there is no separate QA gate.

**Code and review**

- [ ] Code is reviewed and approved by at least one peer and merged to the main branch. Pairing or mobbing on the change counts, since the review happens as the work is done

**Testing**

- [ ] All automated tests pass in the CI/CD pipeline
- [ ] Unit tests cover all new functionality and pass
- [ ] Integration tests are written and pass
- [ ] API automated tests cover at least 80% of the work item's acceptance criteria

**Validation**

- [ ] Acceptance criteria are met and have been validated against the running software
- [ ] No known defects have been introduced

**Documentation**

- [ ] Technical and user-facing documentation is updated where needed

**Deployment and tracking**

- [ ] The change is production-ready and deployable to production at any time, behind a feature flag where needed
- [ ] Azure DevOps work item is updated and closed
- [ ] Release notes or change log updated
- [ ] The appropriate local engineering process has been followed

!!! info "Continuous delivery is the expectation"
    Meeting this Definition of Done means a change can deploy to production at any time. Teams that don't yet deploy straight to production use a staging or QA environment as an interim step, and are expected to keep moving towards continuous delivery over time. The wider engineering standards behind this sit on the [Engineering practice](engineering-practice.md) page, in the 14 Continuous Delivery Markers.

The team reviews its Definition of Done at each retrospective to keep it relevant and current.

### Cross-cutting controls

Cross-cutting controls are legal, safety, or organisational requirements that apply to every work item regardless of type. Unlike the criteria above, these cannot be waived by a team-level exception: they reflect obligations placed on DHCW as an organisation. Where a control does not apply to a given work item, record why on the work item rather than removing the check.

- [ ] Cyber security requirements for the change have been met, including secure handling of any data the change touches
- [ ] User-facing interfaces meet WCAG 2.2 AA accessibility standards
- [ ] User-facing content meets Welsh Language Standards
- [ ] The change meets applicable technical and data standards
- [ ] Clinical safety obligations have been met where the change is in scope (DCB0129 / DCB0160)
