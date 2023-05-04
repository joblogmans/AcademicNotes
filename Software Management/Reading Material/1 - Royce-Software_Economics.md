Reading material lecture 1.


What we have learned over decades of advancing software development best practice is that software production involves more of an economics than an engineering discipline. This paper provides a provocative perspective on achieving agile software delivery and the economic foundations of modern best practices.

Software development focuses on the activities required in the development process. Software delivery focuses on the results of that process. Latter is better.

*Table 1: Differentiating conventional engineering governance from economically driven governance*
| Software Development: Engineering Driven | Software Delivery: Economics Driven |
|-|-|
| Distinct development phases | Continuously evolving systems |
| Distinct handoff from development team to maintenance team | Common process, platform, and team for development and maintenance |
| Distinct and sequential activities from requirements to design to code to test to operations | Sequence of usable capabilities with ever-increasing value |
| Phase and role specific processes and tools | Collaborative platform of integrated tools and process enactment |
| Collocated teams | Geographically distributed, Web-based collaboration |
| Early precision in complete plans and requirements | Evolving precision as uncertainties are resolved |
| Governance through measurement of artifact production and activity completion | Governance through measurement of incremental outcomes, and progress/quality trends |
| Engineering discipline: precisely define requirements/plans completely, then track progress against static plans and scope | Economic discipline: reduce uncertainties, manage variance, measure trends, adapt and steer with continuous negotiation of targets |


Software project managers are more likely to succeed if they use techniques similar to those used in movie production. Consider:
- Most software professionals have no laws of physics, or properties of materials, to constrain their problems or solutions. They are bound only by human imagination, economic constraints, and platform performance once they get something executable.
- Quality metrics for software products have few accepted atomic units. With the possible exception of reliability, most aspects of quality are very subjective, such as responsiveness, maintainability and usability. Quality is best measured through the eyes of the audience.
- In a software project, you can seemingly change almost anything at any time: plans, people, funding, requirements, designs, and tests. Requirements—probably the most misused word in our industry—rarely describe anything that is truly required. Nearly everything is negotiable.
The quality of software is judged more like a beauty contest than by precise mathematics and physical tolerances.

Use standards, construction companies also have standards because it is expensive to badly reinvent physics, same for software. For most products, systems, and services, you want to standardize where you can and not reinvent. Be precise in what you need to be custom/different and how.

Waterfall projects usually report great progress until all code is brought together, then everything falls apart. Continuous progress is impossible. *A software project that has a consistently increasing progress profile is certain to have a pending cataclysmic regression.*

*Hindsight from thousands of software project post-mortems has revealed a common symptom of governing a software project with an engineering management style: the project’s integration and test activities require an excessive expenditure of resources in time and effort. This excessive rework is predominantly a result of postponing the resolution of architecturally significant issues (i.e., resolving the more serious requirements and design uncertainties) until the integration and test phase. We observed that better performing projects would be completed with about 40% of their effort spent in integration and test. Unsuccessful projects spent even more.*

You can't make a five digit precision design without a five digit precision understanding of the problem.

Top 10 Management Principles of Iterative Development:
1. Base the process on an architecture-first approach.
2. Establish an iterative life-cycle process that confronts risk early.
3. Transition design methods to emphasize component-based development.
4. Establish a change management environment.
5. Enhance change freedom through tools that support round-trip engineering.
6. Capture design artifacts in rigorous, model-based notation.
7. Instrument the process for objective quality control and progress assessment.
8. Use a demonstration-based approach to assess intermediate artifacts.
9. Plan intermediate releases in groups of usage scenarios with evolving levels of detail.
10. Establish a configurable process that is economically scalable.

The cheaper/easier/quicker it is to make changes, the more likely they happen, the more likely the product will improve.

Best software practices all have one thing in common: they reduce uncertainty. Uncertainty brings costs. Look at the principles: 1, 2, 3, 6, 8, and 9 all reduce uncertainty. The others? Look at a definition of measurement: *A set of observations that reduce uncertainty where the result is expressed as a quantity.* All the other principles are for feedback and measurements. Reduce uncertainty!

Top 10 Management Principles of Agile Software Delivery:
1. Reduce uncertainties by addressing architecturally significant decisions first.
2. Establish an adaptive life-cycle process that accelerates variance reduction.
3. Reduce the amount of custom development through asset reuse and middleware.
4. Instrument the process to measure cost of change, quality trends, and progress trends.
5. Communicate honest progressions and digressions with all stakeholders.
6. Collaborate regularly with stakeholders to renegotiate priorities, scope, resources, and plans.
7. Continuously integrate releases and test usage scenarios with evolving breadth and depth.
8. Establish a collaboration platform that enhances teamwork among potentially distributed teams.
9. Enhance the freedom to change plans, scope and code releases through automation.
10. Establish a governance model that guarantees creative freedoms to practitioners.

*Understanding the difference between precision and accuracy is a fundamental skill of good software managers, who must accurately forecast estimates, risks, and the effects of change. Precision implies repeatability or elimination of uncertainty. Unjustified precision — in requirements or plans — has proved to be a substantial yet subtle recurring obstacle to success.*