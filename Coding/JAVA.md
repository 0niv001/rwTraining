---
sticker: lucide//coffee
---
## Basics
- Need a Main class, with a main method inside of it. 
- Every Java file, should have the same name class inside of it. 

JVM is the runtime environment, abstraction between code and hardware. Allows for cross platform compatibility

JRE runtime that uses the JVM, core libraries and other components needed to run Java programs. 

Execution sequence
1. Write code
2. Compile it
3. Verify bytecode. 
4. Load classes
5. Execute Bytecode
6. Run in runtime environment
7. Handle exceptions
8. Terminate app. 

If objects have same value it will only use up memory once - new instances point to the object in memory. 
## Best practices
- Use descriptive variable names. 
- Use camel case notation. 
- Try to have exit code 0. 

```java
//Scanner allows to get input
import java.util.Scanner;

//Random is non inclusive, starts at 0
import java.util.Random;

// Main class
public class Main{
	
	// Main method
	public static void main(String[] args){ // can leave out strings[] args
		// for single line comments */ for multiple lines
		
		// TYPE name = assign; for variables
		int x = 400;
		String name = "Niv";
		char y = '@';

		//final creates constants that cannot be changed
		final String NAME = "Niv";

		//Scanner class used to gather input, create new class object
		//Use next.line() to get input twice
		Scanner scanner = new Scanner(System.in);
		String input = scanner.nextLine();
		
		//Can use x++ or x-- to increment or decrement values
		x++;
		x--;
		
		//Syntax for if and else if statements
		if(x > 400){
			x++;
			continue // skip iteration of loop and move to the next iteration. 
		}
		else if(x == 400){
			x--;
		}
		else{
			x*=2;
			
		}
		// ternary if else shorthand
		age = (condition) ? "do this if true" : "do this if not";

		// Switches can be used to test for equality for many cases
		switch(name){
			case "Jack": System.out.print("Not my name");
			// can use """ to write paragraphs on sout
			break; // can use to terminate loops prematurely as well
			default: System.out.print("test");
		}
		// Logical operators: && , || , !
	}
}
```
## Data types and variables
- Primitive (Stored as value) and reference (Stored as reference to memory). 
- Primitive are in the stack. 
- Reference are in the heap, are slower than primitive types.  
- Data type determines amount of memory allocated for storing data. 
- First bit in num data types is the + or - 
- Can easily change data type to another if it  has higher memory allocated to it 
	- byte -> short is fine
	- short -> byte will not work. 
- Float single precision, need to put f at the end of it. 
- Double double precision, twice as many decimal places. 
### Type casting
Take a value and change it to another data type. 
For numbers this can create issues if number is higher than allocated memory, turns + into - 
Make sure to cast within range. 

```java
boolean -> Boolean b = true; // b.CompareTo() 
int -> Integer

String a = "test"; // a then has methods that we can use

short age1 = 2
byte age2 = (byte) age1;
```
#### Math Methods
 - max = largest of 2 numbers
 - min = smallest of 2 numbers
 - sqrt = square root
 - round
 - ceil = rounds up
 - floor = rounds down
## Loops
- Do while loop, performs action at least once, very similar to while loops. 
- For each, used to iterate through elements in an array

```JAVA
while(condition){
	System.out()
}

do {
	System.out()
} while(condition)

for (int i=0; i <=10; i++) {
	System.out
}

for(TYPE i : array ){
	System.out 
}
```
## Arrays and ArrayList
- Normal arrays are fixed in their length. 
``` Java
String[] cars = {"Ferrari","Mclaren","RedBull"}; 
String[] names2 = new String[]{"Niv", "Tom", "Alice", "Bob"}
String[] names3 = new String[7] // empty spaces
String[][] name = {
	{}
	{}
}

ArrayList<String> name = new ArrayList<String>();

array.clone() // 
```
## Methods
- Functions
- Void if you are not returning a value, otherwise write the data type you will return. 
- Access modifiers: Can also be applied to classes and variables. 
	- public - Accessible anywhere in and out of the program.
	- private - Only accessed within the class it is declared in. 
	- protected - Between private and public. access from declared class or subclasses.
	- default - method can be accessed only within package they are declared in. 
- Static
	- Cannot have a static object. ?? Will cover in detail later on in the program. 
- Returns. 
	- Void - if there is no return. 
	- Data type. 
``` Java
public void name(TYPE var, TYPE var){
	 
}
// overloaded methods - share same name but have different parameters, data type and number of parameters are taken into account
```
## Printf
```Java
// souf 
%d - decimal
%b - bool
%c - character 
%s - string
%f - floats and doubles
```
# OOP
- Create objects in different class java files, allowing us to create multiple objects. 
- Create them in the same way you would with scanner or random object. 
- Constructors are methods called when an object is created. 
- Can have overloaded constructors, just like with methods - use instead of default values?
## Principles
- **Abstraction** 
	- Focus on key features to better manage complexity, allows for more efficient and manageable code. 
	- Classes - Cannot be instantiated (cannot create objects from it), it is used as a blueprint for other classes, allows to create hierarchy. 
	- Methods - Do not have an implementation, defined in abstract class. They are implemented in subclasses. 
	- Constructors - Initialise variables common in all subclasses, less duplication. 
- **Interfaces**
	- Way of defining set of methods that class must implement. 
	- Allow separation of definition of data type from implementation
	- Code becomes easier to write, reuse and modular. 
	- Can have as many interfaces into a class, as opposed to single abstract inheritance. 
	- Different rules for different interfaces, hence why they are not implemented in abstract classes. 
	- Define using interface keyword. 
	- Can define constants, and methods are implicitly public and abstract and can't have implementation. 
	- Should be well documented, and public access modifiers, other best practices should be adhered to as well. 
	- 
- **Encapsulation** 
	- Hide irrelevant details in implementation, leaving only important stuff, code is easier to maintain and robust. !! Use access modifiers. 
	- Getters and setters - way to access and modify attributes of an object, allowing for better integrity and security. 
	- use prefix get for getters and set for setters. 
- **Inheritance**
	- Create new classes based on previous ones, less repetition, more organised and modular code. 
	- Parent referred to as superclass, child referred as subclass. 
	- Child inherits properties and methods of superclass, and can have additional ones. 
	- Types of inheritance:
		- *Single*: Inherit from only one superclass (most used type)
		- *Multiple*: Inherit from multiple superclasses. 
		- *Multilevel*: Subclass inheriting from superclass which inherits from superclass before. 
		- *Hierarchical*: Multiple subclasses inherit from single superclass, used to create hierarchy. 
	- Super - Keyword used to refer to super class. Allows access to properties and methods not available from subclass. 
	- *Upcasting*: Casting from subclass to superclass. 
	- *Downcasting*: Casting from superclass to subclass. 
- **Polymorphism** 
	- Use objects of different classes interchangeably, more flexible and reusable code. 
	- Compile time: Method overloading, compiler chooses which method to call. 
	- Run-time: Method overriding, method called is determined at runtime. 
	- Dynamic method dispatch: Call to overridden method is resolved at runtime instead of compile. 
	- Constructors: ensures base and derived classes are initialised correctly

**Constructor best practices**
- Initialise object state- set up all necessary properties, helps avoid errors. 
- No side effects - should not modify external state or produce output. 
- Simplicity and efficiency. 
### Types of methods
- Class - Associated with class
- Static - called on the class itself instead of an instance. , operations that don't depend on state of object. 
- Instance - Called on an instance of the class, used to manipulate instance variables. Can perform operations that depend on the state of the object. 
- Every class extends objects -> can have a whole pathways. 

```Java
public class Car { // use extends to create subclass 
	String att1
	int att 2
	private double att 3 // private makes attribute inacessible outside of class
	
	// Constructor help create different objects, with different attributes
	// Always make constructors public so you can create the object. 
	// Can create default constructor with no attributes
	
	public Car(String att1, int att2, double att3 ....){
		// This is used to assign value to constructor
		this.att1 = att1;
		this.att2 = att2;
		this.att3 = att3;
	}

	void test(){
		System.out.println(this.att1 + "is the first attribute");
	}
	
	// Create getting and setting  method
	public double getAtt3(){
		return att3
	}

	public void setAtt3(double att3){
		this.att3 = att3
	}
	@Override // Overrides OG method, if it has == name, return and parameters
}
Car myCar = new Car();
```
## Exception Handling
- Exceptions are errors during program execution, allowing program to continue. 
- Checked (Checked by compiler) and unchecked (Not checked, detected at run time). 
- Create log of what is causing the exceptions. 
- Multiple exceptions: Can use multiple catch blocks, need to be from most to least specific. 
- Custom exceptions - specific to particular application or program, superclass of exception. 
```java
try {
	//try running code in here without crashing
}
catch (MoreSpecificException e){
	//if there is an error, run this code
}
catch (LessSpecificException){

}
finally { // ensures piece of code is always executed
	//e.g. send out log 
	// not too different from writing the next line
} 
```
## Collections in Java
- Interfaces - Collection/ List, Set, Queue, Map to manipulate groups of objects. 
- Implementation classes. 
- List implementation
	- Array list
		- Store and manipulate dynamic collection, no need to specify ahead of time. 
		- add(), remove(), get()
		- Cannot use primitive data types. 
	- Stack
		- Subclass of Vector - LIFO stack 
		- push(), pop(), peek() - returns item at the top of the stack, without removing it. 
		- Quick access to last item. 
	- Linked List
		- Header (Pointer to first linked element)size (numbers of elements in linked list) and modCount (Modifications made to the linked list)
		- addFirst(), addLast(), removeFirst(), removeLast(), as well as same as arraylist. 
		- "Floating rectangles" dotted around in memory, linked to each other. 
		- Change where items are pointing to. 
		- Much faster and efficient than array list when adding, unless adding to the end. 
		- When searching, you need to go through each one of them. 
		- Good for dataset with less updating. 
- Set Implementation
	- HashSet - 
		- Uses hash table to store unique elements, does not keep order, allows null elements. 
		- Add, Remove - Objects itself instead of the index, Contains method. 
		- Everything is done in constant time, there's no duplicates and therefore no redundant information. 
		- Require more memory
	- LinkedHashSet
		- Doubly linked list running on all elements. 
		- Keeps the order. 
		- Takes up a lot of memory. 
	- TreeSet
		- Sorted order, 
		- Easy to iterate over elements in specific sequence
		- Add, remove, first (First, lowest element in the set) methods. 
		- No null elements. 
```java
ArrayList<Integer> al = new ArrayList<>(); // same syntax for others e.g. Stack
sout(al) -> prints out whole array
sout(al.get(index)) -> to get value of item 

```

- Queue Implementation
	- Priority Q - FIFO (First in, first out)
		- Priority Q based on natural order to custom operator. 
		- Add, remove, peek methods. 
		- Allows for duplicates
	- ArrayDeque
		- Resizable array implementing deque interface
		- You can have any object types inside of it. 
- Maps
	- HashMap
		- Map interface, Key value pairs, only key is unique. 
		- put, get, remove methods 
- Enum Map
	- Used with enum keys
	- put, get, containskey()
	- Good for lists of items. 
	- Whenever on is created, they should be typed in caps. 
- Tree Map
	- Sorted by keys. 
	- Can use binary search for it. 
	- Remove things by their key. 
	- 