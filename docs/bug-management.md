# Bug management

All defects must be documented as bug tickets in Azure DevOps. Every bug goes through a triage process to assess impact, severity, and priority. Quality is a whole-team responsibility: bugs are not failures of the test engineer; they are signals to the whole team about where the system or our process fell short.

## How bugs enter the team

- **Internal testing:** exploratory testing by engineers or test engineers during the sprint
- **Automation:** failures triggered by our automated end-to-end test suites
- **Monitoring and alerting:** system logs, performance spikes, or error-rate alerts
- **External sources:** user support channels, direct feedback from clinical users, or health board stakeholders

## Bug ticket structure

Every bug ticket must contain enough information for the team to replicate and diagnose the problem:

- **Title:** short, descriptive, and specific
- **Steps to reproduce:** written in Given / When / Then format
- **Expected behaviour vs actual behaviour**
- **Evidence:** screenshot, log output, or error message
- **Environment:** which environment the bug was found in

## Triage

After a bug is created, the Product Owner, a Software Engineer, and a Test Engineer triage it together. They agree:

- **Severity:** Critical, Major, Minor, or Trivial – how serious is the defect?
- **Priority:** Immediate, High, Medium, or Low – how urgently must it be fixed?
- **Root cause (once investigated):** code logic, environment configuration, integration issue, or data quality

## Bug routing

Critical and High priority bugs are pulled into the active sprint immediately. The team pauses **all** other work to address them, and **every member** of the team works on the bug until it is fixed (this is called swarming). A capacity buffer for in-sprint bugs is a sensible planning practice.

Medium and Low priority bugs are routed to the product backlog and prioritised by the Product Owner for a future sprint.

|  | P1: Immediate | P2: High | P3: Medium | P4: Low |
| --- | --- | --- | --- | --- |
| **S1: Critical** | Live service crash. Total data loss. Pull into sprint immediately. | Core feature broken. No workaround exists. | Heavy background error. No user impact yet. | Crash on deprecated browser. Low user exposure. |
| **S2: Major** | Major memory leak. Critical security flaw. | Core feature broken. Difficult workaround. | Non-core feature broken. Easy workaround. | Bug affecting less than 1% of users. |
| **S3: Minor** | Broken link on a key page. Significant accessibility failure. | UI misalignment affecting daily workflow. | Slow loading on a minor page. | Minor glitch on an internal tool. |
| **S4: Trivial** | Wrong logo on homepage. | Broken layout on a marketing page. | Typo in a settings menu. | Typo on a draft or internal page. |
