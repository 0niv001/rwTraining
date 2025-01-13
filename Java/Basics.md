- Every Java file should have the same name class inside of it. 
- Use descriptive variable names. 
- Use camelCase notation. 
- Try to have exit code 0. 

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
