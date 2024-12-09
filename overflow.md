In programming, `overflow` occurs when a value computed during an operation exceeds the maximum limit of the data type used to store it. Since the data type can not represent numbers beyong its range, the value "wraps around" to the opposite end of the range, causing incorrect results.
Think of it like a car's odometer that maxes out at 999.999: if the odometer reaches its maximum value and you drive one more mile, it wraps around to 0.

__NOTE__: Java doesn't throw an error or exception for overflow; it just gives the wrapped value.

``` java
public class OverflowExample {
	public static void main(String[] args) {
		int maxValue = Integer.MAX_VALUE; // Max value of int: 2.147.483.647
		System.out.println("Max value: " + maxValue);
	int result = maxValue + 1; // Causes overflow
	System.out.println("Overflow Result: " + result); // Output: -2.147.483.648 instead of 2.147.483.648
	}
}
```