Reading material lecture 2.

*Summarized quickly, skipping things already discussed in other materials.*

# Chapter 2: Software processes
Four fundamental activities in software engineering:
1. **Software specification:** The functionality of the software and constraints on its operation must be defined.  
2. **Software design and implementation:** The software to meet the specification must be produced.  
3. **Software validation:** The software must be validated to ensure that it does what the customer wants.  
4. **Software evolution:** The software must evolve to meet changing customer needs.

Software process models:
1. Waterfall model
2. Incremental model
3. **Reuse-oriented software engineering:** This approach is based on the existence of  a significant number of reusable components. The system development process  focuses on integrating these components into a system rather than developing  them from scratch.

## Reuse-oriented software engineering
Reuse-oriented approaches rely on a large base of reusable software components and an integrating framework for the composition of these components.

The four stages of the process:
1. **Component analysis:** Given the requirements specification, a search is made for components to implement that specification. Usually, there is no exact match and the components that may be used only provide some of the functionality required.  
2. **Requirements modification:** During this stage, the requirements are analyzed using information about the components that have been discovered. They are then modified to reflect the available components. Where modifications are impossible, the component analysis activity may be re-entered to search for alternative solutions.  
3. **System design with reuse:** During this phase, the framework of the system is designed or an existing framework is reused. The designers take into account the components that are reused and organize the framework to cater for this. Some new software may have to be designed if reusable components are not available. 
4. **Development and integration:** Software that cannot be externally procured is developed, and the components and COTS systems are integrated to create the new system. System integration, in this model, may be part of the development process rather than a separate activity.

There are three types of software component that may be used in a reuse-oriented process:
1. Web services that are developed according to service standards and which are available for remote invocation.  
2. Collections of objects that are developed as a package to be integrated with a component framework such as .NET or J2EE.  
3. Stand-alone software systems that are configured for use in a particular environment

## Requirements engineering process
There are four main activities in the requirements engineering process:  
1. **Feasibility study:** An estimate is made of whether the identified user needs may be satisfied using current software and hardware technologies. The study considers whether the proposed system will be cost-effective from a business point of view and if it can be developed within existing budgetary constraints. A feasibility study should be relatively cheap and quick. The result should inform the decision of whether or not to go ahead with a more detailed analysis.
2. **Requirements elicitation and analysis:** This is the process of deriving the system requirements through observation of existing systems, discussions with potential users and procurers, task analysis, and so on. This may involve the development of one or more system models and prototypes. These help you understand the system to be specified.
3. **Requirements specification:** Requirements specification is the activity of translating the information gathered during the analysis activity into a document that defines a set of requirements. Two types of requirements may be included in this document. User requirements are abstract statements of the system requirements for the customer and end-user of the system; system requirements are a more detailed description of the functionality to be provided.
4. **Requirements validation:** This activity checks the requirements for realism, consistency, and completeness. During this process, errors in the requirements document are inevitably discovered. It must then be modified to correct these problems.

Four activities that may be part of the design process because of their significance:
1. **Architectural design**, where you identify the overall structure of the system, the principal components (sometimes called sub-systems or modules), their relationships, and how they are distributed.
2. **Interface design**, where you define the interfaces between system components. This interface specification must be unambiguous. With a precise interface, a component can be used without other components having to know how it is implemented. Once interface specifications are agreed, the components can be designed and developed concurrently.
3. **Component design**, where you take each system component and design how it will operate. This may be a simple statement of the expected functionality to be implemented, with the specific design left to the programmer. Alternatively, it may be a list of changes to be made to a reusable component or a detailed design model. The design model may be used to automatically generate an implementation.
4. **Database design**, where you design the system data structures and how these are to be represented in a database. Again, the work here depends on whether an existing database is to be reused or a new database is to be created.


