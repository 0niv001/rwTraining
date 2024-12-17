---
sticker: lucide//coffee
---
- Every Java file should have the same name class inside of it. 
- Use descriptive variable names. 
- Use camel case notation. 
- Try to have exit code 0. 
## Basics
**Data types**
- Primitive data types are stored as values in memory (Stack)
- Reference data types are stored as reference in memory (Heap). 
- Data types determine the amount of memory allocated for its storage. 
```java
int num1 = 2; //primitive

Integer num2 = 3; //reference
```

*Type casting*
- Can change types to another if changing into higher memory type
	- byte -> short ✅
	- short -> byte ❌
- Careful for stack overflows. 
- Make sure to cast within range. 
```Java
byte age1 = 2;
short age2 = (short) age1;
```

**Variables**
```java
String user = "Niv";
int age = 25;

final String NAME = "Nirvesh"; //This cannot be changed
```

**Print**
- printf - easily print variables. 
```java
%d - decimal
%b - bool
%c - character 
%s - string
%f - floats and doubles
```

**Comments**
- // for single line comments
- \*/ for multiple lines

**Input**
- Import and create new scanner object. 
- Use next.line() to get input twice. 
```java
import java.util.Scanner;

Scanner input = new Scanner(System.in);

String name = input.nextLine();
```

**Random**
- Non inclusive- starts at 0
```java
import java.util.Random;

Random random = new Random();
```

**If statements **
```java
if (condition){
	//do this
}
else if(condition){
	//do this instead
}
else{
	//otherwise do this
}
```

*Ternary shorthand*
```java
int variable = (condition) ? "do this if true" : "do this if not";

//example
int age = 24;
String canVote = (age > 17) ? "You can vote" : "You cannot vote";
```

**Switches**
- Use instead of multiple if else statements when checking equality. 
```java
switch(condition){
	case "" : //do this
	break; // stop running the code
	default: // do this if no matches
}
```

*Enhanced Switches*
```java
String day = "Mon";

switch(day){
	case "Mon", "Tue", "Wed", "Thu", "Fri" -> sout("weekday");
	case "Sat", "Sun" -> sout("weekend");
	default -> sout("Not a day")
}
```
## Loops
**For Loop**
```java
for (int i =0; i <= 10; i++){
	//Do this for this amount of iterations
}
```

**For each**
- Easy way of iterating through collections. 
```Java
for (Type i : iterable){
	// For item in iterable, do this. 
}
```

**While**
```java
while(conditon){
	// Do this while condition is ...
	// Remember to have somethig that changes the condition
}
```

**Do-While**
- Runs code at least once before starting the loop. 
```java
do {
	// Do this
} while(condition)
```

## Array
- Store multiple values in the same variable.
- Fixed in length. 
```java
String[] cars = {"Ferrari", "RedBull", "McLaren"};

String[] cars = new String[3]; //Create array with empty spaces

String[][] nested = {{ }
					 { }}

Object[] name = new Object[3]; // Create array of objects
name[index] = object; // add object to array

```
## Methods
**Type of methods**
- Class: Associated with class
- Static: Called on the class itself instead of an instance. 
- Instance: Called on instance of the class, to manipulate instance variables, performing actions dependent on state of object. 
**Access Modifiers**
- Public: Accessible anywhere in and out of the program
- Private: Only accessed within the class it is declared in. 
- Protected: Between private and public. 
- Default: Method can be accessed only within package they are declared in. 
**Returns**
- Void if there is no return
- If returning add the data type. 
- Add data type for parameters as well. 
```java
public void name(type var){
	// do this 
}

void name(Object objName){} // can pass objects to methods as well 
```

*[[Recursion]]*
- Method calling itself

```
```

**Varargs**
Allow method to accept different num of arguments, put into an array

```java
add(1,2,3,4); // will print out 10

static int add(int... nums){
	int sum = 0;

	for(int sum number : nums){
		sum += number;
	}

	sout(sum);
}
```

**Chaining**
```java
String name = "Niv";

name = name.concat(" M.").toUpperCase().trim(); // NIVM.
```
## OOP
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

## Exception Handling
- Multiple exceptions go from most to least specific. 
- Custom exceptions are specific to programs and are a superclass of exception. 
- Good practice to use specific Exceptions
**Types of exception**
- Checked - By compiler
- Unchecked - Found at run time. 

```java
try{
	//try running this code
}
catch(SpecificException e){
	//If this specfic error do this
}
catch(Exception e){
	//Any other error do this
}
finally{
	//this will always execute after. 
	//good to close any files or scanenrs open
	//can use to create and send over log of error
}
```

## Collections

### List implementation
**Array list**
- Store and manipulate dynamic collection. 
- Have to use reference data types. 

```java
ArrayList<Integer> arrList = new ArrayList<>();

arrList.add(3);

arrList.remove(index);

arrList.get(index);

arrList.set(index, element);
```

**Stack**
- Subclass of vector - LIFO (Last in, First out)
- Quick access to last item. 
```java
Stack<Integer> stack = new Stack<>();

stack.push(1); //Add item to stack

stack.pop(2); //Remove and return first item in stack

stack.peek() //Return item at top of stack without removing it
```

**Linked List**
- *Components:*
	- Header: Pointer to first linked element
	- Size: Number of elements in LinkedList
	- modCount: Modifications made to LinkedList
- Much faster and efficient than ArrayList when adding, unless adding to end. 
- When searching you need to iterate through each one. 
- Good for dataset with less updating. 

```java


linkedList.addFirst();
linkedList.addLast();
linkedList.removeFirst();
linkedList.removeLast();
```

### Set implementation
**Hash Set**
- Use [[Hash Tables]] to store unique elements
- Does not keep order
- Allows null elements
- Operations done in constant time
- Requires more memory

```java

```

**Linked Hash Set**
- Doubly linked list running on all elements
- Keeps order
- Takes up a lot of memory

```java

```

**Tree Set**
- Sorted order
- Easy to iterate over elements in specific sequence
- No null elements

```java
TreeSet<Integer> treeSet = new TreeSet<>();

treeSet.add();

treeSet.remove();

treeSet.first(); //Returns first / lowest element in the set
```
### Queue Implementation
**Priority Q**
- FIFO (First in, First out)
- Based on natural order or custom operator
- Allows for duplicates. 

```java
```

**Array Deque**
- Resizable array implementing deque interface
- Can have any object types inside of it

```java
```

### Maps
**Hash Map**
- Map interface with key value pairs. 
- Key is always unique. 

```java

hash.put()
hash.get()
hash.remove()
```
**Enum**
- Used with Enum keys. 
- Good for ordered list of items in a collection
- Typed in caps

```Java

```

**Tree**
- Sorted by keys. 
- Can use [[Binary Search]]
- Remove values by keys. 

```java

```

## Generics
Allow types to be parameters when defining classes, interfaces and methods. 
1 version for all reference data type. 
Bounded types limit data types you can have

**Methods**
```java
Integer[] intArr = {1,2,3,4,5};
String[] stringArr = {"Niv","Tom","Bob"};

public static <T> void displayArray(<T>[] array){ // allows to pass both arrays
	for(T x : array){
		sout(x)
	}
}

public static <T> T returnGeneric(T[] array){
	return array[0];
}

public static <T extends Number> void onlyNumbers(){} // only takes numbers
```

**Classes**
```java
public class GenericClass <T> { // can also add muliple generics <T,V>
	T value;

	GenericClass(T value){
		this.value = value;
	}
}

IntegerClass<Integer> myInt = new GenericClass<>(1);

StringClass<String> myString = new GenericClass<>("Test");
```
## File class
Abstract representation of file and directory path
Provides methods to check permissions for files and manipulating them. 

**Terminology**
- Streams: Fundamental concept in file IO, Read or write data to file or other data stream, Classified into input and output streams. 
- Readers and writers:  Used for reading and writing character based data from and to streams.
- Buffers: Optimise IO operations, reducing number of reads and writes., temp storage for data that is being read or written. 
- Exceptions: Can result in exceptions such as file not found, permission denied, IO errors.

```java
import java.io.File;

File file = new File("fileName.txt"); // make sure to add file extension

file.exists(); // checks if file exists, NEEDS to be done before operations. 
file.isFile(); // file or folder
file.getPath(); // display path file
file.getAbsolutePath(); // full file path
file.delete();
```

**File Writer**
- Buffered: Used for large outputs. 
- File Writer: Used for smaller files. 
```java
import java.io.FileWriter;
import java.io.IOException;

try{
	FileWriter writer = new FileWriter("fileName.txt");
	writer.write("write this text in the file");
	writer.append("Append this text at the end of the file");
	writer.close();
} catch (IOException e){
	e.printStackTrace();
}
```

**File Reader**
Read content as stream of characters, one by one. 
- File reader: Smaller files 
- Buffered: Efficient reading of large files
```java
import java.io.FileReader;
import java.io.IOException;
import java.io.FileNotFoundException;

try{
	FileReader reader = new FileReader("fileName or Path.txt");
	int data = reader.read() //return int with byte value, if -1 = no more data
	while (data != -1){
		sout((char)data);
		data = reader.read();
	}
	reader.close();
} catch (FileNotFoundException e){
	e.printStackTrace();
} catch (IOException e){
	e.printStackTrace();
}
```

*JSON Libraries*
- JSON.simple : Lightweight library
- Gson: High performance, flexible and easy to use API
- Jackson: Same as Gson. 

*Common exceptions*
- FilNotFoundExceptions
- IOException: General purpose exception due to input or output stream. 
- !! have a log error message. 

Can separate the path name from file name, to allow users to choose the name of the file, can also do this for a file extension. 

Remember to keep file extensions consistent. 

When deleting a file, make sure to prompt the user before deleting, making sure they don't accidentally do it. 

![[Screenshot 2024-12-16 at 11.03.09 am.png]]
## Serialisation
- Converting object into byte stream
- Saves state of the object after the program exits. 
- Can be saved as file (.ser) or sent over a network. 

```java
import java.io.Serializable;

public class User implements Serializable {
	String name;
	String pass;

	public void hello(){
		sout("Hello " + name)
	}
}
```

```java
import java.io.*

User user = new User();
user.name = "Niv";
user.pass = "Test";

try{
	FileOutputStream fileOut = new FileOutputStream("fileName.ser");
	ObjectOutputStream out = new ObjectOutputStream(fileOut);
	out.writeObject(user);
	out.close();
	fileOut.close();
} catch (Exception e){
	sout(error)
}

```

**Deserialisation**
Converting byte stream into an object 

```java


```
## Threads


```java

```

**Multithreading**


# JUnit Testing
