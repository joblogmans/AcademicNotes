24-04-2023

Programming is only a part of software management. You require budgeting, convincing managers, defining the used tools, setting up the requirements, talking with customers, analyzing end-users, managing contractors, etc. This course will focus on the process and the software product itself.

Software management: a high level view *(slide copy)*:
- Attempt to apply traditional engineering practices to software!
- This means that we attempt to control the quality of the software product by managing the software development process
- Management consists of measuring to obtain actual values and possibly actuating with corrective measures
- Important role for measurements (metrics) → by measuring we can infer the software quality
- Important role for modelling the software development process → by modelling the software development process we can understand and manipulate it
- And please note: ‘software engineering’ and ‘programming’ are fundamentally different!

Learn the language of your audience. Reliability and such are not necessarily terms that managers or the press understand. 'Quality' is a very vague concept, even more when talking about software.

In this course, quality is:
1. Conformance to requirements
	1. Sufficient quality if it conforms to its requirements
	2. Implies requirements are clearly specified
	3. Non-conformance means defect
2. Fitness for use
	1. A system is 'of quality' when it is fit for its intended use
	2. Takes customers' requirements and expectations into account

Small q: product works and is reliable. Big Q: includes small q as well as process quality and customer satisfaction.

Total Quality Management:
![[TQM-key-elements-slide.png]]

## Models
Choose appropriate for your situation.

### Waterfall model
- specify what the software should do before writing code  
- breaks the overall process in steps (divide and conquer)  
	- with specified deliverables  
	- and entry and exit criteria  
	- allows tracking of progress  
- forces software modularity  
	- and allows parallel development (teams)  
- documents are generated that facilitate maintenance

This model is very good when requirements are well-known and stable.

![[Prototyping approach.png]]

### Iterative development approach
1. Define a subset of the requirements  
2. Develop a subset of the product that fulfils the requirements  
	-  Covers essential needs of customers  
	- Vehicle for analysis and training  
	- Learning experience for developers  
3. Based on this intermediary product, adjust the design and requirements and iterate.
Customer needs evolve with improved design, feedback and learning.

![[Iterative development process model example.png]]

### Spiral model
- Combines waterfall and prototyping to control risk  
- Software development is performed in consecutive phases:  
	- concept of operation  
	- software requirements  
	- product design  
	- detailed design and implementation  
- each phase has the same sequence of steps:  
	1. Identify objectives (of a product part) and implementation alternatives  
	2. Evaluate alternatives, identify risks and resolve them → prototypes, simulations, models and benchmarks can be used!  
	3. Review involving key members

![[Spiral model.png]]

### Unified Process  
(or Rational Unified Process—RUP)

- Developed by the same guy as UML
- Unified Process is:  
	- Use case-driven
		- Use cases define the functional capabilities of the system to be built and represent the functional requirements of the system  
	- Architecture-centric  
		- Architecture gives a view of the design of the whole system  
	- Iterative and incremental  
		- Iterations are steps in a workflow, increments correspond to growths in functionality

![[Unified Process Overview.png]]

Phases:
1. Inception  
	- Idea for software product defined; project kick off; initial use cases; project risks prioritised  
2. Elaboration
	- Use cases defined; system architecture designed; resources planning; views delivered (use case model, design model and implementation model)  
3. Construction
	- Architecture grows to system; code is developed and tested  
4. Transition
	- Beta testing; defects tracked and fixed; software moves to maintenance team

### Extreme Programming (XP)
- First example of agile
- Concentrate on essential things and leave process burdens out
- Devised to improve software quality and cope with changing requirements
	- Discouragement of early requirements gathering, extensive analysis and design modelling
	- Limits planning for future flexibility ('do not plan what you will not deliver')
- Five cornerstone values: communication, simplicity, feedback, courage, respect

![[Extreme Programming cycle.png]]

### Cleanroom approaches
- Perform software development as an engineering process, instead of try-and-error
- Process based on:  
	- Proof of correctness of design and code  
	- Formal quality certification via statistical testing  
- Experience:  
	- Lower defect rates in first-time execution than industrial average  
	- Mainly applied to small projects  
	- Requires mathematical training of development team!

![[Cleanroom process example.png]]

### Domain/Content-driven processes
- i.e. processes with steps determined by specific domain/purpose/target  
- For example:  
	- object-oriented development processes  
	- model-driven development processes  
	- development process for service-oriented applications  
	- Processes for ERP implementation projects, e.g. AcceleratedSAP for the SAP’s enterprise resource planning systems

## Conclusion
The most suitable process depends on your context. Context can include your type of product, your organization, scale, and the required quality.

## Common responsibilities of software managers
- Proposal writing.  
- Project planning and scheduling.  
- Risk management.  
- Project estimation/costing.  
- Project tracking and reviews.  
- People management.

Where risk management is one of the most important software management tasks in the 21st century.