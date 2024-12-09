## Simple analogy
Think of recursion as standing in front of a mirror that reflects another mirror. Each mirror reflects a smaller image until it eventually becomes too small to reflect anything. That final image is the base case!

Teknikk som kaller seg selv for å løse en oppgave
For eksempel:
``` Java 
int factorial(int n) {
    if (n == 1) {         // Base case: Når vi kommer til 1, stopper vi.
        return 1;
    } else {
        return n * factorial(n - 1); // Ellers, gang tallet med factorial av neste mindre tall.
    }
}

```

Imagine standing in a line of people. Each person asks the person in front of them the same question until the first person at the front has the answer. Then, the answer flows back through the line, person by person.

### Key parts of recursion
1. __Base case__: The condition where the recursion stops. Without this the method would keep calling itself forever.
2. __Recursive case__: The part where the method calls itself, moving closer to the base case.

## Example: Factorial calculation
Factorial of a number `n` (written as `n!`) is the product of all numbers from 1 to `n`.
- __Mathematical definition__:
	- `n! = n * (n - 1)!`
	- Base case: `1! = 1`
``` java
public class RecursionExample {
	public static int factorial(int n) {
	// Base case: factorial of 1 or 0 is 1
	if (n == 0 || n == 1) {
		return 1;
	}
	// Recursive case: n * factorial of (n-1)
	return n * factorial(n - 1);
	}

	public static void main(String[] args) {
		System.out.println(factorial(5)); // Output: 120
	}
}
```

