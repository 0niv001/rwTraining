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

```JAVA
import java.math.BigInteger;

public class Main {
    private static BigInteger[] cache;

    public static void main(String[] args) {
        int iter = 10000;
        int sequence = iter--;
        cache = new BigInteger[iter +1];

        System.out.println(Fibonacci(iter));
    }

    private static BigInteger Fibonacci(int n){
        if (n <= 1){
            return BigInteger.valueOf(n);
        }

        if (cache[n] != null)
            return cache[n];

        BigInteger tempCache = Fibonacci(n-1).add(Fibonacci(n-2));
        cache[n] = tempCache;
        return tempCache;
    }
}
```

**Varargs**
Allow method to accept different num of arguments, put into an array. 
- Can they be used in class constructors. 

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