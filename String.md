> In Java, a `String` is a sequence of characters used to represent text. It is one of the most commonly used data types and is part of the `java.lang` package. Strings in Java are objects, and they are implemented as instances of the `String` classes.
> --- _ChatGPT_

---

## Common String Methods
The `String` [[class]] provides numerous [[method]]s for manipulating and working with strings. Here are some common ones:

| Method                                                   | Description                                            |
| -------------------------------------------------------- | ------------------------------------------------------ |
| `length()`                                               | Returns the number of characters in the string.        |
| `charAt(int index)`                                      | Returns the character at the specified index           |
| `substring(int beginIndex)`                              | Extracts a substring starting from the specified index |
| `substring(int beginIndex, int endIndex)`                | Extracts a substring within a range                    |
| `contains(CharSequence s)`                               | Checks if the string contains the specified sequence   |
| `equals(Object obj)`                                     | Compares the content of two strings for equality       |
| `equalsIgnoreCase(String str)`                           | Compares string, ignoring case differences             |
| `toUpperCase()`                                          | Converts string to uppercase                           |
| `toLowerCase()`                                          | Converts string to lowercase                           |
| `replace(CharSequence target, CharSequence replacement)` | Replaces occurences of a substring                     |
| `trim`                                                   | Removes leading and trailing whitespace                |
| `split(String regex)`                                    | Splits the string into an array based on a delimiter   |