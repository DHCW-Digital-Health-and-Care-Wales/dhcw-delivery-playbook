# Working in the open

DHCW is a public sector organisation, funded by public money to deliver services for the people of Wales. That means the way we work should be as transparent as possible. Working in the open is a principle embedded in the Digital Service Standard for Wales and in how we think about accountability to the public we serve.

Working in the open means that, by default, the artefacts this playbook describes should be publishable. Roadmaps, backlogs, team charters, definitions of done, architectural decisions, and code should all be written as though they will be seen by the public, because in many cases they should be.

## What this looks like in practice

**Open backlogs.** Product teams are encouraged to publish their backlogs and roadmaps where it is safe and appropriate to do so. The WIS vaccination team publishes their backlog openly through Basecamp, giving clinicians, health board colleagues, and the wider public a live view of what the team is working on and why. This kind of transparency builds trust with users and stakeholders and creates a healthier relationship between delivery teams and the people they serve.

**Open code.** Code written with public money should, wherever possible, be public. DHCW teams publish reusable code through the NHS Wales Solutions Exchange on GitHub. Before building something from scratch, teams should check whether a reusable component already exists. Before finishing a piece of work, teams should consider whether what they have built could be useful to another team or organisation. This is the Public Money, Public Code principle in practice.

**Open show-and-tells.** Sprint reviews and show-and-tells should be open to anyone with an interest. While attendees will most often be NHS Wales colleagues, there is no reason to restrict them. Commissioners, third-party suppliers, other UK health bodies, academics, and members of the public have all attended DHCW show-and-tells. An open invitation signals confidence in the work and creates unexpected connections. Teams should publish show-and-tell schedules openly and share recordings where possible.

**Open ways of working.** This playbook is itself an example of working in the open. It describes how DHCW teams work, and it is written to be shareable beyond DHCW. Teams should apply the same thinking to their own working practices: retrospective outputs, team charters, and lessons learned should be written clearly enough to share, not locked in internal folders where no-one can learn from them.

## Our default licence

Publishing code openly works best when the licence is clear from the start. Our default is to release new source code under the MIT licence, and documentation under the Open Government Licence v3.0, unless there's a specific reason to choose otherwise. Add a LICENCE file to a repository when you create it, so anyone who finds the code knows how they can use it.

Where it's safe to do so, develop code in the open from the start of a piece of work, in a public repository, rather than building privately and opening it up at the end. Working this way from day one is simpler than opening a codebase later, and it keeps the history of the work open too.

## What working in the open is not

Working in the open does not mean publishing everything indiscriminately. Personal data, patient information, commercially sensitive supplier details, and security-relevant configuration must be handled with appropriate care and must never be published. The test is not "can we publish this?" but "is there a good reason not to?"

Clinical safety artefacts, information governance documentation, and data processing agreements follow their own governance processes and are not covered by this principle.

## The NHS Wales Solutions Exchange

The NHS Wales Solutions Exchange is the shared GitHub space for reusable code and components across NHS Wales. Teams should:

- Check the Solutions Exchange before building something that might already exist
- Publish reusable components, patterns, and tools when they complete work that others could benefit from
- Write READMEs and documentation as though the reader is from a different organisation, because they might be

## Digital Service Standard for Wales

The Digital Service Standard for Wales explicitly supports open ways of working. Standard 12 requires teams to make their source code open and use open standards. Teams delivering DHCW services are assessed against this standard and should be able to demonstrate how they are meeting it.
