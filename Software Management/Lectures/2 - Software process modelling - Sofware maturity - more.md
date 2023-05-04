02-05-2023

## Software development processes - which to use in what context?
Key software development process philosophies:
- Waterfall
- Iterative/incremental development
- Agile

Definitions:
- **Process**: "*a structured set of activities required to develop a software system*"
- **Specification**: "*definining what the system should do*"
- **Design and implementation**: "*defining the organization of the system and implementing the system*"
- **Validation**: "*checking that it does what the customer wants*"
- **Evolution**: "*changing the system in response to changing customer needs*"
- **Software process model**: "*is an abstract representation of a process. It presents a description of a process from some particular perspective*"
- **Products**: "*outcomes of a process activity*"
- **Roles**: "*responsibilities of the people involved in the process*"
- **Pre- and post-conditions**: "*statements which are true before and after a process activity has been enacted or a product produced*"

Plan-driven and agile processes:
- Plan-driven processes are planned in advance and progress is measured against this plan
- In agile, planning is incremental and easier to change
- In practice, a combination is used

Software process:
- "*Real software processes are inter-leaved sequences of technical, collaborative and managerial activities with the overall goal of specifying, designing, implementing and testing a software system.*"
- Four basic process activities (specification, development, validation, evolution) are organized differently per process.
	- Waterfall has them strictly sequentially
	- in incremental development they are interleaved

Top 10 principles of waterfall development ('engineering management style'): *copy from slide*
1. Freeze requirements before design.  
2. Forbid coding prior to detailed design review.  
3. Use a higher order programming language.  
4. Complete unit testing before integration.  
5. Maintain detailed traceability among all artifacts.  
6. Thoroughly document each stage of the design.  
7. Assess quality with an independent team.  
8. Inspect everything.  
9. Plan everything early with high fidelity.  
10. Control source code baselines rigorously.
Key issues:
- cost of change is high
- amount of rework is high

Top 10 management principles of iterative development: *copy of slide*
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

Top 10 management principles of agile software delivery: *copy of slide*
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

![[comparing-typical-project-schedules-profiles.png]]

## Software process improvement
Goal: improve quality, reduce cost, accelerate development
Approaches: CMMI-based and agile

The approaches in a nutshell:
- Process maturity approach focuses on improving process and project management and introducing good software engineering. Level of process maturity reflects the extent to which good practice has been adopted.
- Agile focuses on iterative development and reduction of overhead in the process.

Process quality and product quality are closely related. Good process is usually required for good product. For manufactured goods, process is the principal quality determinant. For design based activities, other factors are involved, e.g. capabilities of designers.

Factors affecting software product quality:
- Development technology
- People quality
- Cost, time and schedule
- Process quality

Quality factors:
- Large project: development process determines quality
- Small project: capabilities of developers is main determinant
- Small project: development technology is very significant
- All cases: unrealistic schedule -> lower quality

Why process modeling?
- document process for dissemination and standardization
- Allows for reasoning about processes
- Automated support

## How to ensure product quality
Overall quality of management system is important to determine outcome of software projects.
Frameworks for software development processes:
- SEI Process Capability Maturity Model (CMM) and other software process maturity assessment methods

## Process maturity models
Current "standard" is CMMI framework from SEI.
The five levels of CMMI are:
1.  Initial: The software process is ad hoc and disorganized.
2.  Managed: The process is planned, monitored, and controlled.
3.  Defined: The process is well-defined and documented.
4.  Quantitatively Managed: The process is measured and controlled using metrics.
5.  Optimizing: The process is continuously improved based on quantitative feedback.
Assessment relies on questionnaire. Qualification for a level: 90% of key questions and 80% of all questions answered as yes. See [this paper](http://www.sei.cmu.edu/library/abstracts/reports/93tr024.cfm).

Example descriptions of a selection of key elements (KPA) (taken from level 2): *copy from slide*
- **Requirements Management**: "*common understanding between customer and software project of customer's requirements that will be addressed by software project*"
- **Software Project Planning**: "*reasonable plans for performing software engineering and for managing the software project*"
- **Software Project Tracking and Oversight**: "*adequate visibility into actual progress so effective actions can be taken when software project's performance deviates significantly from software plans*"

Two versions of the CMMI model:
- Staged: expressed in terms of capability levels
- Continuous: capability rating computed

Continuous model is finer-grained and allows for using it in more specific needs, as organizations can pick and choose process areas to improve.

![[History-of-CCMs.png]]

## Quality management standards
ISO 9000: set of standards and guidelines for quality assurance management systems. Focus on: "*Say what you do, do what you say, and prove it.*" But does not say anything about actual quality -> improved in ISO 9001:2001.

ISO 9000 elements: *copy of slide*
1. Management responsibility  
2. Quality system  
3. Contract review  
4. Design control  
5. Document control  
6. Purchasing  
7. Purchaser-supplier product  
8. Product identification and traceability  
9. Process control  
10. Inspection and testing  
11. Inspection, measuring and test equipment  
12. Inspection and test status  
13. Control of nonconforming product  
14. Corrective action  
15. Handling, storage, packaging and delivery  
16. Quality records  
17. Internal quality audits  
18. Training  
19. Servicing  
20. Statistical techniques

## Conclusions
- Agile software management:
	- dynamically manage scope, plan and process
	- based on honest measurements and tests
- The quality of the software product can be improved and controlled:
	- by improving and controlling the software development process
- Software development processes can be documented and shared throughout the development teams
- Software development processes and companies can be assessed for their quality by applying generally accepted models

## Measurements for process and product quality
"*You cannot control what you cannot measure*"
Software measurement: deriving numeric values for an attribute of a software product or process. Allows for objective comparisons between techniques, products and processes. There are few established standards in this area.

Software metric: any type of measurement which relates to a software system, process or related documentation (e.g. lines of code, hours required to develop a component). May be used for predictions.

Metrics assumptions: *copy of slide*
- A software property can be measured.
- The relationship exists between what we can measure and what we want to know. We can only measure internal attributes but are often more interested in external software attributes.
- This relationship has been formalised and validated.
- It may be difficult to relate what can be measured to desirable external quality attributes.

Example: *copy of slide*
**Proposition**: *‘the more rigorously the front-end of a software development process is performed, the better the quality of the back-end’*  
**Necessary steps**
1. Define ‘software development process’
2. Define ‘front-end’ and ‘back-end’
3. Define ‘rigorous performance’ in terms of metrics
4. Define ‘quality at the back-end’ in terms of metrics
5. Define testable hypotheses
6. Gather data and test the hypotheses

![[Measurement-example-diagram.png]]

 Problems with measurement in industry:
 - Impossible to quantify ROI of introducing organizational metrics program
 - Few standards for metrics of measurements processes/analysis
 - Often, software processes are not standardized and poorly defined and controlled
 - Most work on software measurement has focused on code-based metrics and plan-driven development processes. However, more and more software is now developed by configuring ERP systems or COTS
 - Introducing measurement adds overhead

Product metrics:
- Quality metric should be a predictor of product quality.
- Classes of product metric:
	- Dynamic: collected by measurements made of a program in execution (e.g. efficiency, reliability).
	- Static: measurements made of the system representations (e.g. complexity, understandability, maintainability).
- Dynamic is usually clode to software quality, static is more indirect.

Often you first need a software process before you can introduce metrics.
Process measurements should be used to assess process improvements, but it should not be the driving factor, that should be the organization objectives.

Measurement surprises:
- Reducing the number of faults in a program leads to increased number of help desk calls
	- Program reaches wider and more diverse market because the product is more reliable.
	- Users might have used the faulty ways and are now confused as their method doesn't work anymore.

Approaches to software measurement:
- Goal-Question-Metric: top-down
	- Goals: what are the objectives?
	- Questions: questions about areas of uncertainty related to the goals, you need process knowledge to derive these.
	- Metrics: measurements to be collected to answer the questions
- Software analytics approach: bottom-up

