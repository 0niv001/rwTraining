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
- Abstraction - Focus on key features to better manage complexity. 
- Encapsulation - Hide irrelevant details in implementation, leaving only important stuff, code is easier to maintain and robust. !! Use access modifiers. 
	- Getters and setters - way to access and modify attributes of an object, allowing for better integrity and security. 
	- use prefix get for getters and set for setters. 

- Inheritance - Create new classes based on previous ones, less repetition and more organised code. 
- Polymorphism - Use objects of different classes interchangeably, more flexible and reusable code. 
### Types of methods
- Class - Associated with class
- Static - called on the class itself instead of an instance. , operations that don't depend on state of object. 
- Instance - Called on an instance of the class, used to manipulate instance variables. Can perform operations that depend on the state of the object. 

```Java
public class Car {
	String att1
	int att 2
	private double att 3 // make attribute inacessible outside of class
	
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

}

Car myCar = new Car();
```
## Try catch
```java
try {
	//try running code in here without crashing
}
catch (Exception e){
	//if there is an error, run this code
}

finally
```

