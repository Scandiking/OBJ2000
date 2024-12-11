>In Java programming, **generics** is a feature that allows you to write flexible, reusable, and type-safe [[code]]. It enables classes, interfaces, and methods to operate on objects of various types while providing compile-time type safety. This reduces the risk of runtime type errors and eliminates the need for explicit type casting. ( ... )
>Generics improve code readability, reusability, and maintainability while ensuring type safety, making Java a more robust programming language
> --- _ChatGPT_

- Bør heller kalle det generisk programmering
- Betyr at algoritmer programmeres på en slik måte at datatypen de skal brukes på defineres på et senere tidspunkt
Hvorfor? 
- Feil kan oppdages ved kompilering og ikke programkjøring

---

1. __Typeparameterisering__: Generics tillater å parameterisere typer, som betyr at du kan definere en klasse, grensesnitt eller metode hvor datatypen den opererer på spesifiseres ved et senere tidspunkt.
``` Java
// En generisk klasse
public class Box<T> {
	private  T item;

	public void setItem(T item) {
		this.item = item;
	}

	public T getItem() {
		return item;
	}
}

public class Main {
	public static void main(String[] args) {
		Box<String> stringBox = new Box<>();
		stringBox.setItem("Hello");
		System.out.println(stringBox.getItem()); // Output: Hello

		Box<Integer> intBox = new Box<>();
		intBox.setItem(123);
		System.out.println(intBox.getItem());
	}
}
```

---

2. __Type safety__: Generisk programmering sørger for typesikkerhet ved kompilering. Dette betyr at du ikke kan sette inn en inkompatibel type inn i en generisk samling eller [[class]]. 
``` Java
// Eksempel (uten generics)
List list = new ArrayList();
list.add("String");
list.add(123); // No error, but might cause issues at runtime
```

``` Java
// Eksempel (med generics)
List<String> list = new ArrayList<>();
list.add("String"); // list.add(123); // Compile-time error
```

---

3. __Elimination of Casts__: Før generics måtte du ofte caste objekter når du hentet dem fra en samling. Med generics er datatypen kjent ved kompilering så kasting er unødvendig.
``` Java
// Eksempel uten generics
List list = new ArrayList();
list.add("String");
String s = (String) list.get(0); // Casting required
```

``` Java
// Eksempel med generics
List<String> list = new ArrayList<>();
list.add("String");
String s = list.get(0); // No casting required
```

---

4. __Generic methods__: Du kan lage metoder som er generiske uavhengige av noen spesifikk klasse eller grensesnitt
``` Java
public static <T> void printArray(T[] array) {
	for (T element : array) {
		System.out.println(element)
	}
}

public static void main(String[] args) {
	Integer[] intArray = {1, 2, 3};
	String[] stringArray = {"A", "B", "C"};

	printArray(intArray); // Prints 1, 2, 3
	printArray(stringArray); // Prints A, B, C
}
```

---

5. __Bounded type parameters__: Du kan restricte typene som kan bli brukt med en generisk klasse eller metode ved å bruke [[bound]]s.
``` Java
public static <T extends Number> double sum(T num1, T num2) {
	return num1.doubleValue() + num2.doubleValue();
}

public static void main(String[] args) {
	System.out.println(sum(10, 20)); // Output: 30.0
	System.out.println(sum(10.5, 20.3)); // Output: 30.8
	// System.out.println(sum("10", "20")); // Compile-time error
}
```