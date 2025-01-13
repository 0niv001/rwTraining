**If statements**
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