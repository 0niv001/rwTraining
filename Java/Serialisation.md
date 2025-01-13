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