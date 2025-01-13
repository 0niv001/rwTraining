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
