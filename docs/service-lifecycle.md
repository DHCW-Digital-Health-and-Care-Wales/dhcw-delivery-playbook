# The service lifecycle

Before a team writes a single line of code, we need to understand what we're building and why. Every DHCW product or service moves through the phases of the agile lifecycle set out in the GOV.UK Service Manual: discovery, alpha, beta, live, and eventually retirement. The Digital Service Standard for Wales expects services to work this way (point 8, iterate and improve frequently). This playbook covers all of them, though the emphasis shifts depending on where you are.

| Phase | What it means |
| --- | --- |
| **Discovery** | Understanding the problem. Who are the users? What do they need? What already exists? Discovery ends with a decision on whether to proceed and in what form. |
| **Alpha** | Testing hypotheses. Build prototypes, test with real users, and find out whether your proposed approach works before committing to full development. Not everything that enters alpha should proceed to beta. |
| **Beta** | Building and iterating. This is where sprint-based delivery begins in earnest. You're building real software, releasing to real users, and using feedback to improve continuously. |
| **Live** | Running a service. The product is in production. The team's focus shifts toward reliability, incremental improvement, and making the service better for users over time. |
| **Retirement** | Every service ends eventually. Closing one well means moving users and their data to whatever replaces it, meeting retention and records obligations, and switching off with the same care used to switch on. The GOV.UK Service Manual's guidance on retiring your service covers how. |

Most of this playbook describes how we work in beta and live. However, the ceremonies, backlog structure, and practices described here apply from the first discovery sprint onward.

!!! info "Research keeps going into live"
    The four phases show where different kinds of work are heaviest. They don't switch off at a phase boundary. User research in particular carries on into live, where real use is the richest source of learning. See [Understanding users and their needs](understanding-users.md).

!!! info "Welsh language and accessibility from the start"
    Under the Digital Service Standard for Wales and Welsh Language Standards, every DHCW service must be designed in Welsh and English from the outset, not retrofitted. Accessibility to WCAG 2.2 AA is a baseline requirement, not a testing concern. Both commitments appear in our Definition of Done and must be planned for from Sprint 0 onward.
