Commonly used to save memory in large arrays or for handling raw data (e.g., files or streams)
``` java
byte smallNumber = 100;
```

- Limited to 8-bit signed integers, so assigning a value outside the range of -128 to 127 will result in a compilation error

- Casting is required when converting from larger data types (e.g. [[Integer type]] or [[long type]]) to [[byte type]] to avoid [[overflow]].

``` java
int largeNumber = 130;
byte smallerNumber = (byte) largeNumber; // Overflow occurs: smallernumber = -126
```

So why use it? 
- Particularly useful when working with memory-critical applications, such as in embedded systems or when large arrays of numbers are needed
## Practical example
``` java
public class ByteExample {
	public static void main(String[] args) {
		byte minValue = -128
		byte maxValue = 127;
		byte sum = (byte) (minValue + maxValue); // Casting to handle overflow
	}
}
```