# Metrics and reporting

We use data to understand team health, improve predictability, and spot bottlenecks. Data is a coaching tool. It is never used to blame individuals or micromanage teams.

DHCW's primary engineering health measures are the four DORA metrics. Sprint metrics such as velocity and burndown are useful planning aids for the team, but they are not the headline measures of delivery health for the organisation.

DORA means DevOps Research and Assessment. DORA is a team at Google Cloud that publish research and assessments on software development. The four metrics are performance measures that the DORA team use to assess performance and have become an industry standard since 2018.

## DORA metrics

| Metric | What it tells us |
| --- | --- |
| **Deployment Frequency** | How often we release to production. High performers deploy multiple times per day. If we can't deploy frequently, we have a pipeline or quality problem. |
| **Change Lead Time** | The time from idea to running in production. Long lead times indicate bottlenecks in review, testing, or deployment. |
| **Mean Time to Recovery (MTTR)** | How quickly we can recover from an incident. Measures our operational resilience. |
| **Change Failure Rate** | The percentage of changes that cause a degradation in service. High failure rates indicate quality or testing gaps. |

## Sprint and flow metrics

These metrics help the team plan and reflect. They should be visible to the team on an ADO dashboard and reviewed at retrospective.

- **Planned to complete:** what the team committed to versus what it delivered
- **Sprint burndown:** daily view of remaining work against the ideal line
- **Cycle time:** the time from a ticket being started to it being done
- **Cumulative flow diagram:** a view of work in each stage over time. Widening bands indicate bottlenecks
- **Velocity:** the average story points completed per sprint over five sprints. The team uses it for its own planning. Never compare it between teams or set it as a target

## Quality metrics

- Number of bugs by severity and detection point (in sprint vs in production)
- Unit test coverage
- Automated test coverage
- Technical debt risk (tracked at the team level)

!!! example "DHCW example – Welsh Immunisation System"
    The Welsh Immunisation System reduced its regression testing runtime from six weeks (manual) to three hours (automated). UI test coverage went from zero to full. Release lead time fell from approximately 90 days to approximately 20 days. These are the outcomes that good engineering practice and healthy DORA metrics produce. They are what we are building towards across all DHCW products.
