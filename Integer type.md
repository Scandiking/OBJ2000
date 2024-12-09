The integer data type referred to as `int` is a datatype used to store whole numbers _without decimal points_. It is a primitive data type and has a size of 4 bytes (32 bits). The ranges it can hold is from -2,147,483,648 to 2,147,483,647.

The default value for `int` variables is `0`.

## Usage
- Commonly used for counters, indices, or when dealing with numbers that do not require decimals. 
``` java
int number = 42;
```

__Mathematical operations__: you can perform arithmetic operations like addition, subtraction, multiplication and division.
``` java
int a = 10;
int b = 5;
int sum = a + b; // sum = 15
```

## Type casting
- if you assign a value that exceeds the `int` range, it will cause an overflow.
- Use explicit casting to convert from other data types, such as `long`, `double` to `int`:
``` java
double pi = 3.14;
int truncated = (int) pi; // truncated = 3
```


## Practical example
 ``` java
 public class IntExample {
	 public static void main(String[] args) {
		 int age = 25;
		 int year = 2024;
		 int totalDays = age * 365
		 System.out.println("You have lived approximately " + totalDays + " days.");
	 }
 }
```

Output:
```
You have lived approximately 9125 days.
```

The `int` datatype is a fundamental building block in Java for working with numerical data in programs. 


