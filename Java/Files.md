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

public static void WriteToFile(String filename){  
    try {  
        FileWriter writer = new FileWriter(filename);  
        writer.write("Write this text in the file");  
        writer.close();  
        System.out.println("File write complete");  
    } catch (IOException e) {  
        System.out.println("IO Exception error");  
    }  
}```

**File Reader**
Read content as stream of characters, one by one. 
- File reader: Smaller files 
- Buffered: Efficient reading of large files
```java
import java.io.FileReader;
import java.io.IOException;
import java.io.FileNotFoundException;

try{
	File f = new File(name);  
	Scanner reader = new Scanner(f);  
	
	while (reader.hasNextLine()){  
	    String data = reader.nextLine();  
	    System.out.println(data);  
	}
	reader.close();
	
} catch (FileNotFoundException e){
	e.printStackTrace();
} catch (IOException e){
	e.printStackTrace();
}
```

**File Creation**

```java
public static void CreateFile(String path){  
    File f = new File(path);  
    try {  
        if (f.createNewFile()){  
            System.out.println("File Created");  
        }  
        else {  
            System.out.println("File not created ");  
        }  
    } catch (IOException e) {  
        System.out.println("Unable to create file");  
    }  
  
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