Layering and partitioning. 

Consider comms protocols between subsystems. 
Look at control flow for particular events. 

Closed architecture - Each layer depends only on the layer below it, resulting in low coupling. Each layer might introduce a speed and storage overhead (bottleneck)

Open architecture - Higher layer can access any layer below it to avoid performance bottlenecks, but this leads to increased coupling, because of extra dependencies. 

Repository architecture - Allows many interfacing components to share the same data, this allows us to add subsystems easily, however repositories can become a bottleneck because of too many queue requests. 

Client server architecture - Computer network model where many clients remotely requests and receive service from centralised host server. Clients needs to know the server but the server does not need to know the client. Server is not affected by changes to the client interface. 

P2P Architecture, commonly used computer networking architecture in which each subsystem has the same capabilities ad responsibilities. In contrast to client-server architecture, it introduces more coupling and control flow hazards, which make it more difficult to implement and maintain. 

In client server architecture the client does not need to know the server. In a broker architecture the client does not need to know where the server is. Instead it communicates with a broker and the broker knows the server it handles. 
## MVC Architecture
- Model, View and Controller. 
	- Model represents the data and business logic 
	- View is a user interface
	- Controller handles the user request. 
- Architecture is more suitable for applications with multiple views for a single data source. 
- Views are registered with the Model, when the Model changes, it will notify all the registered views and allow views to find out the changes and update themselves. 
- Bot view and controller know the Model, but the model is independent of views and controllers. 
