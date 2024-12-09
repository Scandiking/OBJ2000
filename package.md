In Java, a `package` is a way to organize and group related classes and interfaces together. It acts like a folder structure in a file system, helping to keep code organized, manageable, and avoiding naming conflicts between classes.
Think of a package as a __container__ for classes, interfaces, and sub-packages that are related to each other.

## Key features:
1. Organizational tool:
	- Helps group related classes together
	- Makes it easier to locate and use classes in large projects


2. Avoids naming conflicts
	- Classes in different packages can have the same name without conflicts.
	- Example: `java.util.Date` and `java.sql.Date` are two different classes with the same name in separate packages.


3. Access control
	- Provides access control by specifying which classes can be accessed by others (via `public`, `protected`, etc.).


4. Reusability
	- Encourages code reuse by organizing commonly used classes into libraries.

## Summary of Built-in Package groups
| Package Group                       | Purpose                             |
| ----------------------------------- | ----------------------------------- |
| `java.lang`                         | Core classes (auto-imported)        |
| `java.util`                         | Utilities like collections and data |
| `java.io`, `java.nio`               | Input/output, file handling         |
| `java.time`                         | Modern date and time API            |
| `java.net`                          | Networking classes                  |
| `java.sql`, `javax.sql`             | Database access (JDBC)              |
| `java.awt`, `javax.swing`, `javafx` | GUI development                     |
| `java.security`, `javax.crypto`     | Security and cryptography           |
