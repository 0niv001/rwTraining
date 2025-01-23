---
sticker: lucide//leaf
---
## Basics

## Boot
- Initialise project using IntelliJ
- Jar - Executable, embedded version of tomcat
- Dependencies give access to all the technologies of spring boot. 
- Help.md doc with guides on the dependencies chosen. 

**Layered architecture**
- Each layer is responsible for a different technical aspect of the application e.g. web, business, data. 
- Controller - presentation layer, no business logic. 
- Service layer - Contains business logic, does not communicate with DB. 
- Repository - Handles Data. 
- Separation of concerns allows us to swap out layers easily. 

Annotate @SpringBootApplication
Everything is done by convention instead of configuration
Application properties = database init 
Dependency resolution mechanism to pull them. 
@SpringBootApplication - auto config, implements and loads everything. 

**Spring boot properties**
- Can be used to configure application. 
- Look through documentation - data, web, cache, core
- can use yaml for properties file. 
- can provide defaults using :


**Annotations**
@Controller -> Selected class/method is a controller
- Sends HTTP requests and redirect to view.
- Specialisation of component, allowing for auto detection. 
- Need to connect URLs with methods -> 


@GetMapping("URL")
- Connects URL with method when receiving GET request to specified url

@RequestParam
- can have (defaultValue = "") for a default value

Add Model - Map of keys and values in model and add it to request and forward to view destination