# Running a reliable service

Getting a service live is the beginning of its life. Once real people depend on it, our job becomes keeping it working, day and night, and putting it right quickly when something breaks. This chapter covers how we run a service well in live.

Some of the foundations are already in the playbook. The [Engineering practice](engineering-practice.md) chapter sets observability as a baseline (Continuous Delivery Marker 14). The [Delivery plans and risk](delivery-plans-and-risk.md) chapter covers rollback and monitoring before go-live. This chapter joins those up into how we operate.

## You build it, you run it

The team that builds a service is the team that runs it. When the people who write the code also carry responsibility for it in live, they build it to be reliable, because they're the ones who get the call when it isn't.

Running a service in live is real work, and it needs to be planned and resourced like any other work. Time has to be set aside for it, rather than squeezed in around new features. A team in live is still a team with a job to do.

## See what's happening: observability

You can't run a service you can't see. Observability is how a team knows what its service is doing in production, and how it finds out why when something goes wrong. Three things do most of the work:

- **Logs** record what happened.
- **Metrics** show how the service is behaving over time: traffic, errors, latency, saturation.
- **Traces** follow a single request through the system, so you can find where it slowed down or failed.

Build these in as you build the service (see Marker 14). Good observability turns a long outage into a quick fix, because you can see the problem instead of guessing at it. Set up alerts on the signals that matter, so the team hears about a problem from its monitoring before a user reports it.

## Set service level objectives

A service level objective (SLO) is a clear target for how the service should perform: how often it's available, and how fast it responds. An SLO turns "the service should be reliable" into something you can measure and hold, like "the booking service is available 99.9% of the time".

SLOs are useful because they make trade-offs explicit. They tell the team when to spend effort on reliability and when it's fine to focus on features. Set targets that reflect what users actually need. Chasing perfect uptime everywhere costs a great deal and rarely helps the user more than a sensible target would.

## Handle incidents

Things will go wrong. A good incident process means they go wrong safely and briefly. Everyone on the team should know:

- How an incident is raised, and who's responsible while it's running.
- How you communicate during one, to users and to the people who need to know.
- How you restore service first, and dig into the root cause afterwards.

Two measures tell you how you're doing: how often incidents happen, and how long they take to put right (mean time to recovery). Bringing recovery time down usually matters more to users than chasing zero incidents, because fast, calm recovery is what they feel.

After a significant incident, hold a blameless review. The aim is to learn what let it happen and fix that, so the same thing can't bite twice. People speak openly when they trust the review is there to improve the system and won't be used to blame anyone.

## Offer a clear support model

Users need a way to get help and report problems, and the team needs those problems to reach it. A support model sets out how issues flow from a user to the people who can fix them, who handles what, and how urgent things get escalated. Link it to bug management (see [Bug management](bug-management.md)) so live issues are triaged and swarmed properly.

## Plan for the worst: disaster recovery and business continuity

Sometimes the failure is big: a data centre goes down, a critical dependency fails, a region goes offline. Disaster recovery is the plan for getting the service back when that happens. For services that clinicians and patients depend on, teams should know how they'd recover, how long it would take, and how much data they could lose in the worst case. Write the plan down, and test it. You only find out whether a recovery plan works by running it.

!!! info "Reliability is designed in"
    The choices that make a service reliable, such as observability, sensible targets, a tested recovery plan, and a team that runs what it builds, are made during design and build, and maintained for as long as the service runs.
