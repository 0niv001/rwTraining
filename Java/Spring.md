---
sticker: lucide//leaf
---
[[Java- Notes]] Framework

## Basics

## Boot
- Initialise project using IntelliJ
- Jar - Executable, embedded version of tomcat
- Dependencies give access to all the technologies of spring boot. 
- Help.md doc with guides on the dependencies chosen. 
- Works out the box

**Gradle**
- Settings define global properties. 
- Build - Defines config for building the project
- Gradlew (Mac/Unix) and gradlew.bat (Windows) - scripts to invoke wrapper, to download installation locally. 
- Gradle repo - Wrapper subdirectory checks version / Downloads distribution. 
	- .jar
	- Properties - 
- bootRun - runs gradle wrapper and builds project
- See Gradle from notification panel in IntelliJ

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