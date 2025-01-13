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

**Custom Exceptions**
```java
public class CustomException extends Exception{
	public CustomException(){}

	public CustomException(String message){
		super(message)
	}
}
```
