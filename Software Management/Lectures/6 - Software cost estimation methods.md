## Estimation techniques
Why use cost estimation models? At least they taught us:
- Writing less code helps
- Reuse helps
- Quality of personnel is important
- Tools help

Still useful to reason about the cost and schedule implications of their software decisions.

Examples of investment decisions that go beyond budgets and schedules:
 - When to develop? Reuse? Purchase?
 - What legacy systems to phase out? Modify?
 - Negotiations of cost/schedule/performance
 - Software risk management decisions
 - Software process improvement decisions (e.g. CMM level, ISO, buying tools)

### Techniques
- Experience-based techniques
	- Estimate of future effort is based on the managers experience of past projects and the application domain.
- Algorithmic cost modeling
	- A formulaic approach is used to compute the project effort based on estimates of product attributes (e.g. size, process characteristics, staff experience)

| Method | Strengths | Weaknesses |
| --- | --- | --- |
| Expert judgement | Assessment of representativeness, interactions, exceptional circumstances | No better than participants. Biases, incomplete recall |
| Estimation by analogy | Based on representative experience | Representativeness of experience |
| Price to win | Often gets the contract | Generally produces large overruns |
| Top-down | System level focus. Efficient | Less detailed basis, less stable |
| Bottom-up | More detailed basis. More stable. Fosters individual commitment | May overlook system level costs. Requires more effort |

### Example: Delphi method
- Iterative group process allows experts to make forecasts without meeting face-to-face
- 5-10 experts who make the forecast
- Staff personnel assist by preparing, distributing, collecting, and summarizing a series of questionnaires and survey results
- After three or four passes through this process, a consensus forecast typically emerges

## Algorithmic cost modelling
$$Effort = A*Size^B*M$$
- Where A is an organisation-dependent constant,
- B reflects the disproportionate effort for large projects and
- M is a multiplier reflecting product, process and people attributes

Most commonly used product attribute for cost estimation is code size.

Several factors influence the final size:
- Use of COTS (Commercial off-the-shelf) and components
- Programming language
- Distribution of system

## Sizing metrics and methodologies
Artifacts: requirements, inputs, outputs, classes, use cases, modules, scenarios
- Often weighted by relative difficulty
- Easy to count at initial stage
- Estimates may differ based on level of detail

Function Points (IFPUG in this case, but others are similar):
- Define boundary of a system
- Use basic counting components of five types:
	- Number of input types (EI): enters, reads
	- Number of output types (EO): prints, exports
	- Number of enquiries (EQ): queries
	- Number of internal logical files (ILF): files internal to the system
	- Number of external interface files (EIF): information that is taken from outside but is not maintained in the system

FP analysis:
- Advantages:
	- Independent of technology and implementation
	- Can be measured early in project lifecycle
	- Can be applied consistently across projects and organizations
- Disadvantages:
	- Difficult to automate
	- Require technical experience and estimation skills
	- Difficult to count size of maintenance projects

## Probabilistic methods
### PERT (Putnam and Fitzsimmons, 1979)
- 3 estimates: optimistic, most likely, pessimistic
- $Expected Size = \frac{optimistic + 4*(most Likely)+pessimistic}{6}$

### COCOMO 2 model
- Empirical model based on project experience
- Not tied to specific software vendor
- Sub-models:
	- Application composition model: used when software is composed from existing parts
	- Early design model: used when requirements are available but design has not yet started
	- Reuse model: used to compute the effort of integrating reusable components
	- Post-architecture mode: used once the system architecture has been designed and more information about the system is available

#### Early design model: multipliers

$$PM = A * Size^{B}* M$$
$$ M = PERS* RCPX*RUSE*PDIF*PREX*FCIL*SCED$$
Where $A=2.94$ and $1.1 \leq B \leq 1.24$

| Multiplier | Description |
| --- | --- |
| RCPX | Product reliability and complexity |
| RUSE | The reuse required |
| PDIF | Platform difficulty |
| PREX | Personnel experience |
| PERS | Personnel capability |
| SCED | Required schedule |
| FCIL | The team support facilities |

The Post-architecture level uses the same formula, but with 17 multipliers instead of the previous 7.

#### The exponent term
M is based on 5-scale factors, their $\frac{sum}{100}$ is added to $1.01$.

| Scale factor | Explanation |
| --- | --- |
| Precedentedness | Reflects the previous experience of the organization with this type of project. Very low means no previous experience; extra-high means that the organization is completely familiar with this application domain. |
| Development flexibility | Reflects the degree of flexibility in the development process. Very low means a prescribed process is used; extra-high means that the client sets only general goals. |
| Architecture/risk resolution | Reflects the extent of risk analysis carried out. Very low means little analysis; extra-high means a complete and thorough risk analysis. |
| Team cohesion | Reflects how well the development team knows each other and work together. Very low means very difficult interactions; extra-high means an integrated and effective team with no communication problems. |
| Process maturity | Reflects the process maturity of the organization. The computation of this value depends on the CMM Maturity Questionnaire, but an estimate can be achieved by subtracting the CMM process maturity level from 5. |

See this table:

![[Scale factor estimation table.png]]

Calendar time can be estimated using a COCOMO 2 formula:
$$ TDEV = 3*PM^{0.33+0.2*(B-1.01)}$$
The time required is independent of the number of people working on the project. Staff required can't be computed by dividing the development time by the required schedule, the more people who work on the project, the more total effort is usually required.

