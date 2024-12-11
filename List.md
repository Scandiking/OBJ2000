`java.util.List`

An ordered collection (also known as a sequence). The user of this interface has precise control over where the list each element is inserted. The user can access elements by their integer index (position in the list), and search for elements in the list.

Unlike sets, lists typically allow duplicate elements. More formally, lists typically allow pairs of elements e1 and e2 such that e1.equals(e2), and they typically allow multiple null elements if they allow null elements at all. It is not inconceivable that someone might wish to implement a list that prohibits duplicates, by throwing runtime exceptions when the user attempts to insert them, but we expect this usage to be rare.[^1]

Since `List` is an interface, it cannot be instantiated directly, but it can be implemented by classes like [[ArrayList]], `LinkedList`, `Vector`, or `Stack`. 

## Key Characteristics of `java.util.List`
1. __Ordered__: Elements are stored in the order in which they are inserted
2. __Index-based__: Each element in the list is associated with an index starting from `0`. 
3. __Duplicates allowed__: A `List` can contain duplicate elements

---

## Common implementations of `List`
- Backed by a dynamic array
- Good for random access due to indexing
- Not synchronized (not thread-safe)
- Slower for insertions or deletions in the middle of the list

``` Java
import java.util.ArrayList;
import java.util.List;

public class Example {
	public static void main(String[] args) {
		List<String> names = new ArrayList<>();
		names.add("Alice");
		names.add("Bob");
		System.out.println(names); // Output: [Alice, Bob]
	}
}
```

----

What is the difference between `List` and `ArrayList`?
Think of it like this:
`List` is a job description. "We need a collection that can add, remove, and access items in order". `ArrayList` is an employee who specializes in doing that job efficiently with arrays. `LinkedList` is another employee who does the same job but specializes in linked lists. When you declare something as a `List` you are saying "I don't care how you do the job as long as you fulfill the `List` contract". When you declare something as an `ArrayList` you are saying "I specifically want this job done the `ArrayList` way".

| Aspect         | List                                                                    | ArrayList                                                   |
| -------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------- |
| Type           | Interface                                                               | Class (implements `List`)                                   |
| Instantiation  | Cannot be instantiated directly                                         | Can be instantiated directly                                |
| Implementation | Provides a contract (method signatures)                                 | Concrete implementation using dynamic arrays                |
| Flexibility    | Allows for different implementations (`ArrayList`, `LinkedList`, etc.). | Specifically tied to a resizable array                      |
| Usage          | Typically used as a reference type to leverage [[polymorphism]]         | Used when the dynamic array behavior is specifically needed |




---

[^1]: https://docs.oracle.com/javase/8/docs/api/java/util/List.html