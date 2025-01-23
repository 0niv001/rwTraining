---
sticker: lucide//rotate-cw
---
*Software Development lifecycle*
- Methodology for software development. 
- Aims to quickly and efficiently make high quality software. 
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

| Technical                            | Financial             | Alternatives       | Operational | Legal                       | Other              |
| ------------------------------------ | --------------------- | ------------------ | ----------- | --------------------------- | ------------------ |
| Do we have resources and tech needed | Cost benefit analysis | Market positioning | Performance | GDPR                        | Risk assessment    |
| Is tech stable and established       | Account for time      | USP                | Information | ISO/IEC                     | Environmental      |
| Risk management                      | Future costs          | Dependencies       | Economy     | Copyright and Design patent | Collection of info |
|                                      |                       |                    | Efficiency  |                             |                    |
|                                      |                       |                    | Services    |                             |                    |
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

| Security                            | Reliability                                    | Continuity                                               | Scalability                  |
| ----------------------------------- | ---------------------------------------------- | -------------------------------------------------------- | ---------------------------- |
| Ongoing process ensuring [[CIA]]    | Does it do what it's meant to?                 | What's needed to keep operations going                   | Can you keep up with demand  |
| Developed with security in mind     | Does not account for repairs                   | How long will software run without crashing              | Physical - hardware,         |
| Planned and managed throughout SDLC | Accounts for time taken for components to fail | Collect info on resources needed to support organisation | Intangible - Business growth |

| Performance                                 | Availability                       | Supportability                            | Serviceability                      |
| ------------------------------------------- | ---------------------------------- | ----------------------------------------- | ----------------------------------- |
| What the system does and how well           | Timely and reliable access to info | Support over lifecycle at reasonable cost | Early detection of problems         |
| Determined as result of functional analysis |                                    |                                           | How easily system can be maintained |
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
- Context diagram
- [[UML]]

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

| Functional Design                                    | Non Functional design           |
| ---------------------------------------------------- | ------------------------------- |
| Fit for purpose according to functional requirements | Quality aspects of system       |
| Logical flow of systems                              | Performance attribute of system |
| Inputs and otputs                                    | Ensure good UX                  |
| Data organisation                                    |                                 |
| Business and processing rules                        |                                 |
| How things appear to users                           |                                 |
**Components**

| Software architecture                                  | UI                                | Infrastructure                              | Ergonomics                                       |
| ------------------------------------------------------ | --------------------------------- | ------------------------------------------- | ------------------------------------------------ |
| Structure of systems an creating them                  | Human Computer Interaction (HCI)  | Software object interaction with components | Software design                                  |
| Software elements, relations and properties among them | Use of input devices and software | Separation of concerns                      | Determination of user needs and interface desing |
|                                                        |                                   | Defined interface                           | User centred approach                            |
|                                                        |                                   | Encapsulate functionalities                 |                                                  |
*Operational Processes*

| Primary lifecycle - Waterfall | Cross Lifecycle                               |
| ----------------------------- | --------------------------------------------- |
| Discovering requirements      | Planning project                              |
| Designing solutions           | Estimating                                    |
| Constructing solutions        | Tracking and reporting status                 |
| Validating solutions          | Defining processes and standards              |
| Implementing solutions.       | Measuring and monitoring process performance  |
|                               | Training                                      |
|                               | Controlling versions and release of software. |

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
## Code development

| Concurrency model    | Tracking                               | Traceability                      | Peer Review                                |
| -------------------- | -------------------------------------- | --------------------------------- | ------------------------------------------ |
| Shared mutable state | [[Jira]]                               | Can be mandated                   | Detect and correct defects in artefacts    |
| Actor model          | Tools to help identify requirements    | Keep track of lifecycle           | Prevent leakages                           |
|                      | Divide requirements into smaller tasks | Indicate dependency between items | Find bugs early, teach and share knowledge |
|                      |                                        |                                   | [[Agile]] retrospective                    |

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

*Levels of testing*

| Unit ->                                        | Integration ->                                | System ->                             | Acceptance ->                     | Regression                              |
| ---------------------------------------------- | --------------------------------------------- | ------------------------------------- | --------------------------------- | --------------------------------------- |
| Test individual software components            | Units combined and tested as group            | Test complete and integrated software | Ensure fit for purpose            | Testing program after modification      |
| Validate each unit (Smallest part of software) | Expose faults in integrated unit interactions | Evaluate compliance with requirements | Test system under typical use     | Ensure defects have not been introduced |
| One of a few inputs and a single output        | Test drivers and stubs are used to assist.    |                                       | Establish confidence in system    |                                         |
|                                                |                                               |                                       | Delivery and deployment readiness |                                         |

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
	- State transition diagram - Transition from one state to another because of input conditions, leading to different events and results in an output. 
- Experienced based 
	- Use expertise to identify key areas to test. 

**Approaches to testing**
- Dynamic and heuristic
- Consultative
- Model based approach
- Risk based
- Methodical
- Standard compliant approach

**Independent testing**

| Benefits                                    | Drawbacks                               |
| ------------------------------------------- | --------------------------------------- |
| Defects seen in neutral perspective         | Outdated documentation references       |
| Unbiased                                    | Can hinder communications               |
| See what's been built, not what dev thought | Devs might be irresponsible for quality |
| No assumptions regarding quality            |                                         |
**Use case testing**
- Identify test cases that cover entire system, on a transactions

**Debugging**
- Reproduction - try to recreate the bug. 
- Allows you to find the problem and submit a fix. 
- Bugs are discovered as code is created
- Use logging - recording feedback when software is being used. 

**Test coverage**
Metric measuring amount of testing performed by a set of test
Structural or white box
Value covered as a %
Different coverage measures.
## Deployment
- Implementation planning
- Training users and operations
- User documentation
- Build software releases
- Deploy software

**Implementation planning**

**User Documentation**
- Instructional material. 
- Training material. 
- Documentation for product or service provided to the end users.
- Designed to assist end users to use the product or service. 

**Build**
- Developed application for the customers that is given by dev team to testing team
- Release is official launch of application for customers. 
- Build when tested and certified by the software testing team is provided to the customers as release. 

Software deployment includes all the processes required for prepping software app to run and operate in environment. 
Involves installation, config, testing and making changes to optimise performance. 
Can be deployed automatically and manually. 

**Config Management**
- Engineering process for establishing and maintaining consistency of product's performance, and attributes.
- Verifies that system performs as intended, and is identified and documented. 

**Implementation Strategies**
- Parallel run: Client uses new and legacy system at the same time. 
- Big Bang: 
	- Complete implementation at once, moving everything to new system.
- Phased Approach: Adoption of new app happens in phases over time, difficult to do if using a waterfall method. 

**Releases packages**
- Alpha: First phase of testing, generally white box techniques. 
- Beta: Follows alpha, features complete, but with a few known bugs. 
- Major / Minor: Software upgrade, gives unique version names or numbers e.g. 15.2

**Version numbering system**
X.Y.Z -> Major.minor.patch
- Major is for significant changes, minor is for smaller updates, patches are small bug fixes. 

**Software licensing**
- Proprietary: Lic
- End User - EULA
- Open Source. 


## Maintenance
4 Main classes
1. Adaptive - Modify system to cope with changes in env
2. Perfective - Implementing new or changed user requirements to enhance the software
3. Corrective - Diagnosing and fixing errors, e.g. those found by users. 
4. Preventive - Increasing software maintainability or reliability to prevent problems in the future. 

Activities
- Minor enhancements
- Major enhancements
- Error correction: Fix errors to make sure software stays useful. 
- Temp workaround: Bypass a problem 
- Performance improvement: Scalability, test if performance requirements are being achieved. 
- Routine updates and upgrades - Fix bugs, Improve performance, protect against risks. 

Reasons for change:
- Changed user requirement
- Problem or incident identified. 
- Regulatory or mandatory change. 
- Infrastructure and platform change. 

Incidents differ from both problems and requests. 
Incident interrupts normal service. 
Problem is identified through a series of multiple incidents with the same symptoms. 

Regulatory change. 

Infrastructure or platform change:
- Windows to Linux
- APIs
- Hardware to Cloud

SLA:
- Agreement between service providers, not a legal contract, Critical part of tech vendor contract. 
- Level of service expected from a vendor. 

Reports, Auto Logs
First and second line support. 

Problem solving techniques
- Brainstorming
- Fault tree analysis
	- Top down approach to identify all potential causes leading to a defect
	- Each cause is broken down into least possible events or faults. 
	- Analysis begins with major defect. 
	- All events are identified
	- Events are traced down to lowest possible level
- Root Cause analysis
	- KT methodology
	- Problem is disconnected from the decision. 
	- What happened? Why? how should we act?
- Ishakawa diagrams
	- Cause and effect diagram.
	- Used to categorise problem in order to identify root causes
- Decomposition
	- Breaking problem down into smaller components. 
	- Break system down into subsystems. 

**Importance of managing and controlling changes**
- Needs and requirements change during lifecycle of the system. 
- Change management ensures evolution of system is controlled. 
- Process of analysing costs and benefits of proposed changes. 

Change process flow:
- Request for change submitted - Change control form. 
- RFC template to record the change.  
- Change assessment and planning. 
- Change approvals. 
- Change implementation. 

Software development plan is a comprehensive composite artefact that gathers all info needed to manage the project. 

Encloses several artefacts developed during inception phase and is maintained throughout the project. 

Plan core components:
1. Scope statement
2. Critical success factor
3. Deliverables
4. Wrok breakdown structure
5. Schedule
6. Budget
7. Quality
8. HR Plan
9. Stakeholder List
10. Comms
11. Risk register
12. Procurement plan. 

Traceability Matrix
- Forward Traceability - Project progresses according to plan
- Backward Traceability - Ensures project stays on track
- Bi-Directional - Combination of forward and backward traceability, tracks and ensures test coverage. 

Elements of deployment or implementation plan
- Info about system support
- Issue tracking
- Escalation processes
- Roles and responsibilities before, during and after deployment. 

## Methodologies
- Waterfall - Sequential design process, wait for one process to be done before going to next.

*Advantages*
- Provide more confidence of what will be finally delivered earlier in cycle
- Large scale design or analysis is required. 
- Where there are many interfaces and dependencies outside of basic product development. 

*Disadvantages*
- Many organisations and people don't find defining requirements easy to do. 
- Comms can be a far higher risk. 
- Tend to be made of teams within teams. 

Main principles of waterfall approach:
- Low customer involvement.
- Strong documentation.
- Sequential structure.