- Allows for creation of objects in different class files. 
- *Constructors*
	- Methods called when an object is created.
	- Can be overloaded. 
	- Should have no side effects - No outputs 
	- Should set up all necessary properties. 
```java
public class Car{
	public String make;

	//Constructor - Always make it public 
	public Car(String make){
		this.make = make; 
	}
	//Default constructor with no attributes
	public Car(){}
}
```

**Inheritance**
- Create new classes based on previous ones allowing for less repetition. 
- Parent class referred to as superclass. 
- Children referred to as subclass. 
- Child inherits properties and methods of superclass and can have additional ones. 
- super - used to refer to super class, allowing access to its properties and methods. 
*Types of inheritance*
- Single: inherit from only one superclass (most used type). 
- Multiple: inherit from multiple superclasses. 
- Multilevel: subclass inheriting from superclass which inherits from another superclass. 
- Hierarchical: multiple subclasses inherit from single superclass. 

*Override:* If method in sub is also in super, we need to use @override for it to work
*Super:* Super class of the object

```java
public class Vehicle{
	double speed;
	void go(){sout("This vehicle is moving")}

	Vehicle(double speed){
		this.speed = speed;
	}
}
```

```Java
public class Car extends Vehicle{
	byte doors; // separate attribute from vehicle
	car.go() // inherits method from Vehicle class

	@Override // Overrides go method from Vehicle superclass
	void go(){
		sout("This car is moving")
	}

	// Use super keyword to pass attribute to superclass
	Car(byte doors, double speed){
		super(speed);
		this.doors = doors;
	}
}
```

**Abstraction**
- Focus on key features to better manage complexity, allowing for more efficient code. 
- Classes: Cannot be instantiated, used as blueprint for other classes allowing hierarchy. 
- Methods: Do not have implementation, but implemented by subclasses. 
- Constructors: Initialise variables common in all subclasses. 
```java
public abstract class Vehicle{
	abstract void go(); // Cannot add body to it 
}
```

```java
public class Car extends Vehicle{
	@Override
	void go(){sout("The car is moving")}
}
```

**Polymorphism**
- Ability of object to identify more than one type. 
- Constructors ensure base and derived classes are initialised correctly. 
- *Compile time:* Method overloading, compiler chooses which method to call. 
- *Run time:* Method overriding, method call is determined at run time. 
- *Dynamic method dispatch:* Call to overridden method is resolved at run time. 

```java
// if all classes extend from the same superclass (Vehicle)
Vehicle[] racers = {car, bycicle, boat}
```

**Encapsulation**
- Hide irrelevant details leaving only what is needed. 
- Allows for security
- Use access modifiers (Public / Private / Protected / Default)
- Use getter and setters to access and modify attributes. 

```java
public class Car{
	private String make; // attribute is inaccessible outside class 
		
	//Use Setters in contructor 
	Car(String make){
		this.setMake(make);
	}
		
	//Getter
	public String getMake(){
		return make 
	}
	
	//Setter
	public void setMake(String make){
		this.make = make;
	}
}

Car myCar = new Car(); // Creates new car object
```

**Interfaces**
- Defines set of methods that class must implement. 
- Can have as many interfaces into a class as opposed to single abstract inheritance. 
- Defined using interface keyword. 
- Can define constants
- Methods are implicitly public. 
- Should have public access modifiers. 

```java
public interface Swim {
	void swim(); // Method does not need body
}
```

```java
public interface Eat{
	void eat();
}
```

```java
public class Fish implements Swim, Eat{

	@Override // need to override interface method
	void swim(){
		sout("The fish is swimming")
	}

	@Override
	void eat(){
		sout("The fish is eating")
	}
}
```

**Lambda**
- Anonymous method
- Class with only one method

```java
@FunctionalInterface
public interface FuncInterface{
	public void message(String name);
}
```

```java

FuncInterface myInterface  = (x) -> {
	sout("This is the message");
	sout("This is a message for " + x);
}

myInterface.message("Niv")
```
