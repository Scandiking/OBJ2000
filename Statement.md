> A _statement_ in Java is a single instruction executed by the [[JVM]]. Statements form the building blocks of Java programs and can perform actions such as variable assignments, method calls, loops, or condition evaluations. Each Java statement typically ends with a semicolon `;`, except for block statements or control flow structures.
> --- _ChatGPT_

### Best practices
- Keep statements concise and readable
- Avoid overly complex nested statements for better maintainability
- Group related statements in blocks for clarity

### Notes
- Statements can span multiple lines but must always conclude properly with a semicolon or closing brace
- Logical errors in statements (e.g., incorrect conditions) will not be caught by the compiler, so thorough testing is essential

- [[Import statement]]
- [[While loop]]
- [[For loop]]
- [[If else]]

### Examples

1. Expression statement
``` java
int x = 10; // Assignment
System.out.println(x); // Method call
```

2. Control flow statement
``` java
if (x > 5) {
	System.out.println("x is greater than 5");
}
```

3. Looping statement
``` java
for (int i = 0; i < 5; i++) {
	System.out.println(i);
}
```

4. Block statement
``` java
{
	int y = 20;
	System.out.println(y);
}
```




