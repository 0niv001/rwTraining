Used to encapsulate the construction of product and allows it to be constructed in steps. 


**Flexible Design**
- Flexible data structure to allow for variations
- Sequence of complex steps. 

**Why use it?**
- Encapsulate creation in an object
- Client uses builder to construct the structure for it. 

*Benefits*
- Encapsulates how complex objects are constructed. 
- Objects can be constructed in multistep and varying process. 
- Hide internal representation of product from client. 
- Product implementation can be swapped in and out because client only sees abstract interface. 

**Example of when to use Builder pattern**
- Used for building composite structure -- What does that mean?
- Creating objects requires more domain knowledge of client than when using a factory. 

Creational design pattern. 

Produce different types types and representations of an object using the same construction process. 

Constructor calls can be ugly and overloaded, as well as causing unnecessary code. 

Extract object construction or creation code out of class and move it to objects called builders. 

Build method returns instance of the class we want to build. 

No need to worry about null values. 

Inner class - private access. 
Force users to instantiate objects using builder. 

Repeated code can be extracted to separate class called Director, as to not write more code when creating objects with similar characteristics. 

Director defines order in which we should call construction steps so we ca reuse certain configurations of the products we are building.  Directors are optional. 

Separate construction of object from representation of it. 
Have setters for the properties of the class. 
Have method called build that returns the object. 
The OG class takes builder as an argument. 

Once you use the build function the builder becomes the object. 

Director takes builder as parameter. can have method for set specification for the object. 

have validation when calling the build method, to make sure values are there


? Use builder class for users in final project

constructor in the object will be private, so users cannot directly call it and will have to make use of the builder. 

allows us to skip optional fields
easier to assign the right properties
can add new fields without breaking code

can have builders with required fields

 potential to mix up unconditional fields as they lose their names. 

Interface chaining can be used to guide user through builder in a specific order

Massive benefit when we need certain properties to be validated before setting them. 

Can we not use varargs for this instead

