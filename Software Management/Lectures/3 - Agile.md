09-05-2023

- Focus on code rather than design
- Based on iterative approach
- Deliver working software quickly and evolve quickly to meet changing requirements
- Limit documentation -> reduce overhead + quick response to changing requirements

Applicability:
- Product development for small/medium-side product for sale
- Custom system development within an organization, where there are not a lot of external rules and regulations that affect the software
- Because of the focus on small, tightly-integrated teams, there are problems in scaling agile method to large systems

Problems:
- Can be difficult to keep the interest of customers
- Team members may be unsuited to the intense involvement
- Prioritizing changes can be difficult where there are multiple stakeholders
- Maintaining simplicity requires work
- Contracts may be a problem due to the flexible nature of agile

Maintenance:
- most orgs spend more on maintaining existing software than they do on new software development -> agile needs to support maintenance as well
- Two issues:
	- Are agile systems maintainable, given the emphasis on development and minimal formal documentation?
	- Can agile methods be used effectively for evolving a system in response to customer change requests?
- Expensive problems may arise if original development team cannot be maintained.

Issues:
Most project include elements of plan-driven and agile processes, balance depends on:
- Is detailed specification and design important?
- Is incremental delivery with rapid feedback strategy realistic?
- How large is the system?
- What type of system is being developed (e.g. real-time systems, need more planning)?
- What is expected system lifetime (long lived need more design documentation for the support team)?
- What devtools are available (agile requires good tools)?
- How is the dev team organized? (spread out may need more design docs to keep consistent)
- Cultural or organizational issues (engineering company may only want waterfall)?
- Quality of the designers and developers? (real coding is designing which is hard, agile requires constant designing)
- System subject to external regulation?

## Extreme programming:
- Perhaps best-known and most widely used agile method
- Extreme approach to iterative development
	- New versions may be built several times per day
	- Increments are delivered to customers every two weeks
	- All tests must be run for every build
- Full-time customer engagement with the team
- People not process -> pair programming, collective ownership, process that avoids long working hours
- Maintaining simplicity through constant refactoring
- Not design for change (changes cannot reliably be anticipated), instead uses constant refactoring

Refactoring:
- Dev team make improvements even without an immediate need for them
- Better understandability = less docs needed
- Some changes require architecture refactor which is more expensive

Pair programming:
- Helps develop common ownership and spreads knowledge
- Informal review process as there is always someone else looking
- Encourages refactoring as whole team can benefit from this
- Measureents suggest that development productivity with pair programming is similar to that of two people working independently
- Two devs at same workstation
- Dynamic peers so all team members work with each other
- Sharing of knowledge reduces risk of member leaving

## Scrum
Scrum approach is a general agile method, but focuses on managing iterative development instead of specific agile practices.
Three phases:
- **Initial phase:** outline planning phase, set general objectives, design architecture
- **Sprint cycles:** each cycle develops an increment
- **Project closure:** wraps up the project, completes docs, and reflection on lessons learned

Sprints are fixed length (usually 2-4 weeks), every sprint is a potential release. Starting point for planning is product backlog. During sprint the team is isolated from customer and organization, scrum master is only point of communication. Scrum master protects dev team from external distractions. End of sprint: work review and presentation to stakeholders.

Scrum master is facilitator who arranges daily meetings, tracks backlog, records decisions, measures progress and communicates with customers and management.

Whole team attends short daily meetings for sharing information, describe progress, risen problems, planning for the following day -> everyone knows what is going on.

Benefits of scrum:
- Product broken down into smaller chunks
- Unstable requirements do not hold up progress
- Whole team have visibility on project -> better communications
- Customers see on-time delivery of increments and gain feedback on product
- Trust between customers and developers is established.

## Scaling agile methods
- Large systems are usually collections of separate communicating systems -> every agile team develops a different system.
- Large systems are 'brownfield systems' which interact with a number of existing systems. Many of the requirements are concerned with this interaction and thus don't really lend themselves to flexibility and incremental development.
- Where several systems are integrated to create a system, a significant portion of development is concerned with system config instead of original code development.
- Large systems have a long procurement and dev time -> difficult to maintain coherent teams with good knowledge about the project
- Large systems usually have a diverse set of stakeholders. Impossible to involve all stakeholders in the dev process.

**Scaling up:** using agile methods for developing large software teams that cannot be developed by a small team
**Scaling out:** how agile methods can be introduced accross a large organization with many years of software dev experience

When scaling, important to maintain agile fundamentals.

For large systems development: not possible to focus only on code. Requires more up-front design and system documentation. Teams require regular communication with other teams. Continuous integration is practically impossible, however, it is essential to maintain frequent system builds and regular releases.

![[Disciplined agile delivery cycles.png]]

## Disciplined agile delivery
DAD supports a robust set of roles:
- **Team lead:** agile process expert, keeps team focused on goals, removes impediments.
- **Product owner:** owns product vision, scope and priorities.
- **Architecture owner:** owns the architecture decisions and technical priorities, mitigates key technical risks.
- **Team member:** cross-functional members that deliver the solution.
- **Stakeholder:** includes stakeholders, but also other stakeholders such as sponsors, devops, architecture, database groups, governance bodies.

DAD manifesto:
- Individuals and interactions over processes and tools
- Consumable solutions over comprehensive documentation 
- Stakeholder collaboration over contract negotiation
- Responding to change over following a plan

![[Scaling agile.png]]


