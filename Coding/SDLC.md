---
sticker: lucide//rotate-cw
---
*Software Development lifecycle*
- Methodology for software development. 
- Aims to quickly and efficiently make high quality software. 

Steps
1. Feasibility study (Can it be built)
2. Requirements analysis()
3. Design
4. Implementation
5. Testing
6. Deployment
7. Maintenance
## Feasibility study
- How development is initiated when a need or opportunity is identified
- Purpose and main activities of a feasibility study. 
- Importance of planning software development
- Purpose of business case
- Benefits from using operational software
- Short focused study
	- Does it contribute to objectives
	- Can it be implemented within time and budget constraints
	- Can it be integrated with other systems
- You either can and cannot do it
- Provides documentation that the idea was investigated. 
- What is the likelihood that this is calm to do. 

*Technical feasibility*
- Do you have the resources and tech to accomplish the task. 
- Is the technology stable and established. 
- Need to be able to manage risks. 

*Financial*
- Cost benefit analysis. 
- What the cost is likely to be later on due to different factors. 
- Put time into your cost analysis. 

*Collection of info*
- Set collection goals early. 
- Well defined metrics and models - Keep them consistent
- Can have big time costs

*Risk assessment

*Consider Alternatives*
- Market positioning
- USP 
- What are the alternatives available. 
- External sources - Careful with dependencies. 

*Operational*
- Performance
- Information
- Economy
- Control
- Efficiency
- Services

*Environmental*

*Legal feasibility*
- Copyright, Designs and Patents Act 1988

**Report Writing**
- Intro / Executive Summary
- Background - Give it some life
- Outline of project
- Methodology / Method analysis
- Overview of alternatives
- Conclusion
- Recommendations
## Requirements
- Requirements help communicate and define customer needs and problems
- Stakeholders can establish consensus on what problems need to be solved. 
- Helps give estimate for timelines. 

**How research can help understand end users**
- Who they are
- Problem they face

**Personas**
Characters created from research to represent different users.   
Helps understand user needs and behaviours. 
Helps you get a different perspective. 

**Customer Journey Mapping**
- Visual representation of experience customers have
- Steps
	1. Nail down user persona
	2. Understand who customers are
	3. Understand goals
	4. Map out user touch points
	5. identify pain points
	6. Prioritise and fix roadblocks
	7. Update and improve. 

**Functional requirements**
- Requirements representing core functionality of system. 

**Non-Functional requirements**
- Additional requirement e.g. Time and performance constraints. 
- Security
	- Ongoing process, ensuring [[CIA]]
	- Software needs to be developed with security in mind. 
	- Should be planned and managed throughout SDLC process. 
	- Need more than tech to ensure security. 
- Availability
	- Timely and reliable access to info and ability of use. 
- Reliability
	- Does it do what it's meant to do?
	- Does not account for repairs that might take place. 
	- Accounts for time taken for components to fail whilst in operation. 
- Performance
	- What the system does and how well it needs to do it. 
	- Should be determined as result of functional analysis looking at customer needs. 
- Capacity
	- Measurable property of a process to the spec. 
		- Number of stories - Future vs past
		- Number of sprints - Future vs past
- Continuity
	- What's needed to keep operations going. 
	- Collect info on resources needed to support organisation. 
	- How long will the software run without crashing?
- Supportability
	- Support software over its lifecycle at reasonable cost. 
	- Have a wiki in place for final project!!
- Serviceability
	- How easily systems can be maintained and repaired. 
	- Early detection of problems is critical. 
- Scalability
	- Can you keep up with volume of demand?
	- Physical - Hardware, data storage, network bandwidth.
	- Intangible - Business growth, can be intrinsic and extrinsic.

**Good requirements**
- Unambiguous
- Testable
- Clear
- Feasible
- Independent
- Atomic - Single thing. 
- Necessary

**Data Dictionary**
- Allows for research to be repeated easily by allowing others to understand data. 
- Explain what all the vars and vals mean. 
- Things to include:
	- Var names
	- Measurement units
	- Allowed values
	- Definition of vars. 

**Tools for requirements gathering**
- Functional decomposition
	- Break down problem in simpler subtasks. 
	- Functional requirement doc is a txt representation of functional decomposition. 
- Use case diagram
	- Dynamic or behaviour diagram in UML
	- Model functionality of system using actors and use cases. 
- Context diagram
- UML
	- 14 Diagram types representing structure, behaviour and interaction of system.
	- ERD 
	- Sequence
	- Activity diagram - Dynamic aspect of systems. 


!! Most important part of the requirements is the contract - Makes sure you get paid and all parties agree on the requirements for the software. 
## Design
- Purpose and scope of design
- Make software fit for purpose according to function and non functional requirements.
- Identify system components that need to be considered when designing software. 
- Good design = Better operational software and impact on costs. 
- Prototyping and modelling to help analysis and design. 

Software design document - Description of design of system to allow for development
2 Stages:
- Preliminary - System and data architecture. 
- Detailed - in depth data structures and algorithms.

**Functional Design - Verb**
- Fit for purpose according to functional requirements
- Logical flow of systems
- Inputs and outputs
- Data organisation
- Business and processing rules
- How things appear to users

**Non-Functional - Attribute**
- Quality aspects of system. 
- Performance attribute of software system
- Ensure good UX

**System components**
- Software Architecture
	- Structures of software systems and creating these. 
	- Each structure comprises software elements, relations and properties among them. 
	- Follow Arrow to make sure that UML is conforming to the standards. 
- UI
	- How users and computer systems interact. 
	- Use of input devices and software. 
	- Figma Mockup. 
- User ergonomics
	- Software design, instead of hardware design. 
	- Determination of user needs, interface design, User support and usability testing. 
	- User centred approach to the development of interactive systems. 
- Infrastructure
	- Software object - interacts with other components
	- Encapsulate certain functionality or set of them
	- Defined interface, conforming to recommended behaviour
	- Separation of concerns. 
	- Requirements often align to whole part. 
- Operational processes
	- Lifecycle
	- Cross lifecycle
	- Primary lifecycle process - Phases of waterfall method
		- Discovering requirements
		- Designing solutions
		- Constructing solutions
		- Validating solutions
		- Implementing solutions
	- Cross lifecycle process 
		- Planning project
		- Estimating 
		- Tracking and reporting status
		- Defining processes and standards
		- Measuring and monitoring process performance
		- Training
		- Controlling versions and release of software
- Measures and metrics
	- Measure of software characteristics. 
	- Important for performance and planning. 
	- Should be:
		- Simple and computable
		- Consistent (Units, objective)
		- Easy to calibrate
		- Easy and cost-effective to obtain
		- Can be validated for accuracy and reliability. 
	- Scope:
		- Cost and effort. 
		- Productivity measures and model. 
		- Data collection. 
		- Quantity models. 
		- Reliability. 
		- Evaluation of methods and tools. 
- HCI (Human computer interaction)
	- User
	- Computer itself
	- How it all works together

## Code development
Concurrency model
- Shared mutable state
- Actor model

Tracking
- Allows flexibility
- Tools help teams identify requirements and divide them into several smaller tasks. 
- Learn [[Jira]]- High demand

Traceability
- Can be mandated. 
- Keep track of lifecycle and what happened. 
- Indicates dependency between items. 

Peer Review
- Detect and correct defects in artefacts and prevent leakage. 
- Find bugs early, teach and share knowledge, consistent design. 
- Agile retrospective - Reflect on iteration, identify actions for improvement. 

## Testing
- Defects can be found throughout the phases of SDLC
- Start early to minimise defects in later stages. 
- Design review, unit testing, regression testing. 

Risk reduction 
- Impact and likelihood.  
- Decide which and if testing is required for certain features. 

Conformance
- % of adherence to pre set expectations. 

All defects start with an error, reviewers need to find defects, and testers know that software contains bugs. 

Debugging and testing are different
- Debug is the dev activity identifying cause of a defect, and fixes that 

Levels of testing
- Unit
	- Individual components of software are tested. 
	- Validate each unit (Smallest testable part of software) performs as expected. 
	- One of a few inputs and a single output. 
- Integration
	- Units are combined and tested as a group. 
	- Expose faults in interaction between integrated units. 
	- Test drivers and stubs are used to assist in Integration Testing. 
- System
	- Complete and integrated software is tested. 
	- Evaluate compliance with specified requirements.  
- Acceptance
	- Establish confidence in system and characteristics of it
	- Does what it is meant to do. 
	- Ensuring fit for purpose - Is it ready for deployment and delivery. 
	- Test of system under typical use. 
- Regression
	- Testing old program after modifying it, ensuring defects have not been introduced. 

**Techniques**
- Functional 
	- What system needs to do, to achieve objectives. 
	- External behaviour, so it is black box testing
- Non Functional
	- Constraints on functionality - How well
	- Security, Performance, Usability (How easily users can use the app, alpha and beta testing), Reliability. 
- Black box
	- Functional and non functional. 
	- External view of software, not using info RE/ internal structure of components. 
	- Derive and select test conditions, cases and data. 
	- Equivalence partitioning - !Not a good model to work from. 
	- Boundary value test - At least 2 test for each of the expected value. 
	- Decision tables - Condition and action stubs and entries. 
- White box
	- 