# Delivery plans and risk

## Delivery plans

A delivery plan is the checklist of everything beyond the code that has to be true before a feature is safely live: dependencies, training, rollback, monitoring, safety sign-off. It lives in Azure DevOps Delivery Plans, next to the work itself, so the team sees each feature's path across sprints without maintaining a separate document. It is a de-risking tool for a product team.

### Development

- Keep the plan in Azure DevOps Delivery Plans so each feature's path across sprints is visible next to the work
- Once a sprint, check it against the dates that actually matter: assessment dates, campaign starts, contract deadlines

### Dependencies

- External APIs and integration readiness
- Third-party vendor timelines
- Security assurance and clinical safety review schedules
- Infrastructure provisioning and environment changes

### Go-to-market and operational readiness

- User documentation and training for clinical and operational users
- Feature flag configuration and rollout plan
- Rollback procedure documented and tested
- Service desk triage pathway agreed with the service management team

### Quality and monitoring

- Feature-level regression testing complete
- Load testing where appropriate
- Monitoring and alerting configured before go-live
- Clinical safety review completed where required (DCB0129 / DCB0160)

## RAID management

The RAID Log is a shared record of the variables that could pull delivery off track. It is owned by the Delivery Manager but maintained by the whole team. Keep it live and up to date.

| Type | Definition | What to do with it |
| --- | --- | --- |
| **Risk** | A potential future event that could knock delivery off course. | Assign an owner. Define a mitigation. Review at each retrospective. |
| **Assumption** | Something we believe to be true that we haven't yet verified. | Validate it as early as possible. If it proves false, reassess. |
| **Issue** | An active problem that is blocking or slowing delivery now. | Escalate immediately. The Delivery Manager is accountable for resolution. |
| **Dependency** | A deliverable from another team or supplier that we need to complete our work. | Track it explicitly. Name the owner in the other team. Flag if it slips. |

## Decision logs

Decisions can be tracked in a **decision log**. We recommend using GitHub for these, as decisions can then be published publicly so everyone can see why we arrived at a decision, whether it is on the design of a feature, the scope of a discovery, or the prioritisation of a feature.

A useful reference is Joel Parker Henderson's [decision-record](https://github.com/joelparkerhenderson/decision-record) repository, which sets out how to initiate and complete decisions for teams, organisations, and systems.
