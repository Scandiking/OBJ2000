In Java, an __InputStream__ is a class from the `java.io` [[package]] that represents an abstract stream of data for reading. It is designed to read data __byte by byte__ from a source, such as:
- a file
- a network connection
- an array
- System input (e.g. keyboard input)

## Key features
1. __Abstract class__: `InputStream` is an abstract class, meaning you cannot create an object of it directly. Instead, you use its subclasses.
2. __Reads data byte by byte__: It reads one byte at a time, making it suitable for binary data like images or files.

## Examples
__1. FileInputStream: reads data from a file__:
``` java
FileInputStream fileStream = new FileInputStream("example.txt");
```



__2. ByteArrayInputStream: Reads data from a byte array__:
``` java
byte[] data = {65, 66, 67};
ByteArrayInputStream byteStream = new ByteArrayInputStream(data);
```



__3. BufferedInputStream: Buffers input for more efficient reading__:
``` java
BufferedInputStream bufferedStream = new BufferedInputStream(new FileInputStream("example.txt"));
```



__4. ObjectInputStream: Reads objects from a stream (used for object serialization)__:
``` java
ObjectInputStream objectStream = new ObjectInputStream(new FileInputStream("objectFile.dat"));
```