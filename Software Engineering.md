**To read - Bennet Book**
- 6.1 - 6.5
- Chapter 6 (6.5, 6.7) 
- Chapter 12, 13.5
- Chapter 14
- Chapter 15 
### Methodologies
- Waterfall
- Incremental
- Prototyping
- Spiral
- Unified Process
### UML
- Structure Diagrams
	- Class
	- Activity
	- State Machine
- Behaviour Diagrams
	- Use case
	- Activity
	- State Machine
- Interaction Diagrams
	- Sequence
	- Communication
- Object Constraint Language (OCL): Formal language used to describe expressions on UML models. 
### Design Patterns
- Singleton pattern
	- Ensures that only one instance of a class is created. 
- Composite patterns
- State pattern
	- Behaviour patterns
### MVC Architecture
- Model, View and Controller. 
	- Model represents the data and business logic 
	- View is a user interface
	- Controller handles the user request. 
- Architecture is more suitable for applications with multiple views for a single data source. 
- Views are registered with the Model, when the Model changes, it will notify all the registered views and allow views to find out the changes and update themselves. 
- Bot view and controller know the Model, but the model is independent of views and controllers. 

## Patterns and Frameworks

Designs that have recurring class/object structures. 

OOP Pattern is an abstraction of a small group of classes that is likely to be helpful over and over again. 

**Software architecture patterns**
Layering and partitioning. 

Consider comms protocols between subsystems. 
Look at control flow for particular events. 

Closed architecture - Each layer depends only on the layer below it, resulting in low coupling. Each layer might introduce a speed and storage overhead (bottleneck)

Open architecture - Higher layer can access any layer below it to avoid performance bottlenecks, but this leads to increased coupling, because of extra dependencies. 

Repository architecture - Allows many interfacing components to share the same data, this allows us to add subsystems easily, however repositories can become a bottleneck because of too many queue requests. 

Client server architecture - Computer network model where many clients remotely requests and receive service from centralised host server. Clients needs to know the server but the server does not need to know the client. Server is not affected by changes to the client interface. 

P2P Architecture, commonly used computer networking architecture in which each subsystem has the same capabilities ad responsibilities. In contrast to client-server architecture, it introduces more coupling and control flow hazards, which make it more difficult to implement and maintain. 

In client server architecture the client does not need to know the server. In a broker architecture the client does not need to know where the server is. Instead it communicates with a broker and the broker knows the server it handles. 

**Software Design Patterns**






**Agile Development**
Light weight development model. 
Best suited for smaller and medium sized business systems. 

Core principles:
1. Focus with working software than documentation - Working software
2. Focus on customer collaboration over contract negotiation - Customer Collaboration
3. Focus on responding to changes over following a plan - Responding to change
4. Individuals and interactions 

**Extreme Programming:**
Still has planning and design phases that focus on coding and testing. 
Overall process is iterative and incremental. 
User story:
- Each story is up to 3 sentences long, written by customer with priority value. 
- If story takes more than 3 weeks then it's too big and needs to be split
- Stories can be added, modified and deleted. 
Only Class responsibility collaboration cards are used (CRC). 
Write code after the unit test
Pair programming. 
Code is continuously integrated with existing code via TDD.
Easier to make changes with TDD and refactoring
TDD:
- Run all tests again to avoid regression to preserver system behaviour 

*Criticisms*
- Rejects proven engineering techniques. 
- Lacks documentation. 
- Lacks formal design - No complex diagrams and specifications
- Complicates contract negotiations. 

**Prototyping**
- Something that can be built quickly in order to explore certain aspects of the systems. 
- Not intended as part of the final system, used as part of other life cycle. 
- Can be used to clarify user requirements
- Construct UI using rapid dev env and send it for evaluation. 


**Spiral**


**Unified Process**
- Make use of UML 
- Iterative
