<cite>A class should use the `private` modifier to hide its data from direct access by clients. This makes the class easy to maintain. Provide a getter method only if you want the data field to be readable and provide a setter method only if you want the data field to be updateable. For example, the `Rational` class provides a getter method `numerator` and `denominator`, but no setter method, because a `Rational` object is immutable.</cite>

<cite>Data field encapsulation: Making data fields private protects data and makes the class easy to maintain</cite>

The data fields `radius` and `numberOfObjects` in the `Circle` class in Listing 9.6 can be modified directly (e.g. `c1.radius = 5` or `Circle.numberOfObjects = 10` ). This is not a good practice - for two reasons:
1. Data may be tampered with. For example, `numberOfObjects` is to count the number of objects created, but it may mistakenly set to an arbitrary value (e.g. `Circle.numberOfObjects = 10`).
2. The class becomes difficult to maintain and vulnerable to bugs. Suppose that you want to modify the `Circle` class tho ensure that the radius is non-negative after other programs have already used the class. You have to change not only the `Circle` class but also the programs that use it because the clients may have modified the radius directly (e.g., `c1.radius = -5`).

To prevent direct modifications of data fields, you should declare the data fields private, using the `private` modifier. This is known as _data field encapsulation_.