`java.util.ArrayList` is part of the Java Collection Framework and provides resizable array implementation. An `ArrayList` can grow or shrink dynamically as elements are added or removed. It is one of the most commonly used classes for handling collections of objects in Java.

| Advantages                                           | Disadvantages                                                                               |
| ---------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Flexible and easy to use for dynamic lists           | Slower than arrays for primitive data types e.g. `int` because it uses objects (`Integer`). |
| Provides a rich set of methods for list manipulation | Not thread-safe (requires external synchronization for concurrent use).                     |
| Built-in support for generics ensures type safety    |                                                                                             |

---

## Common uses cases
- Managing a list of items (e.g. fruits)
- Dynamic arrays where the size isn't fixed or known in advance
- Storing collections that need frequent addition/removal of elements

---

## Key features of `ArrayList`:
1. __Dynamic resizing__:
	- Automatically grows when elements are added beyond its initial capacity
	- Shrinks when elements are removed  
	  
1. __Indexed access__:
	- Elements are stored in contiguous memory locations and accessed via their index.  
	  
1. __Non-synchronized__:
	- Not thread-safe by default. For thread-safety, use `Collections.synchronizedList()` or other alternatives like `CopyOnWriteArrayList`.  
	  
1. __Allows duplicates__:
	- Supports duplicate elements  
	  
1. __Generic support__:
	- Can hold objects of a specific type (type safety) or objects of any type using raw types (not recommended).   

---

## Common methods of `ArrayList`
Here are the commonly used methods in `ArrayList`

| Method                      | Description                                                    |
| --------------------------- | -------------------------------------------------------------- |
| `add(E element)`            | Adds an element to the list                                    |
| `add(int index, E element)` | Inserts an element at a specifix index                         |
| `get(int index)`            | Retrieves the element at the specified index                   |
| `set(int index, E element)` | Replaces the element at the specified index with a new element |
| `remove(int index)`         | Removes the element at the specified index                     |
| `remove(Object o)`          | Removes the first occurrence of the specified element          |
| `size()`                    | Returns the number of elements in the list                     |
| `isEmpty()`                 | Checks if the list is empty                                    |
| `contains(Object o)`        | Checks if the list contains the specified element              |
| `clear()`                   | Removes all the elements form the list                         |
| `toArray()`                 |                                                                |

---

## Example usage
``` Java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        // Create an ArrayList of strings
        ArrayList<String> fruits = new ArrayList<>();

        // Add elements
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");

        // Access elements
        System.out.println(fruits.get(1)); // Output: Banana

        // Modify an element
        fruits.set(1, "Blueberry");
        System.out.println(fruits); // Output: [Apple, Blueberry, Cherry]

        // Remove an element
        fruits.remove("Cherry");
        System.out.println(fruits); // Output: [Apple, Blueberry]

        // Check size
        System.out.println("Size: " + fruits.size()); // Output: Size: 2

        // Check if contains
        System.out.println(fruits.contains("Apple")); // Output: true
    }
}

```

