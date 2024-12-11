A class defines the properties and behaviors for [[object]]s, such as [[StringBuilder]] and [[StringBuffer]].

A __class__ in Java is a blueprint for creating objects. It defines the properties (fields) and behaviors (methods) that an object of the class can have.

## Key characteristics
- Encapsulation of data and methods
- Can include constructors, fields, methods, and nested classes ([[superclass]], [[subclass]])
- Serves as the foundation for object-oriented programming (OOP).

## Syntax
``` java 
public class ClassName { 
	// Fields (attributes) 
	int field; 
	
	// Constructor 
	public ClassName() { 
		// Initialization code 
	} 
	
	// Methods (behaviors) 
	public void methodName() { 
		// Method code 
	} 
}
```

## Example:
``` Java
public class Car {
	// Fields (attributes)
	String brand;
	int speed;

	// Constructor
	public Car(String brand, int speed) {
		this.brand = brand;
		this.speed = speed;
	}
	
	// Method
	public void accelerate() {
		speed += 10;
		System.out.println(brand + " is accelerating. Current speed: " + speed)
	}
}
```