The __JVM__ (Java Virtual Machine) is an integral part of the Java Runtime Environment that enables Java programs to run. It is a __virtual machine__ that provides a runtime environment to execute Java byte code, regardless of the underlying hardware or operating system.
The JVM is responsible for converting the Java byte code (compiled `.class` files) into machine code that the host system can execute. This "write once, run anywhere" capability is what makes Java platform-independent.

1. __Loading__:
	- The JVM loads `.class` files into memory. 
	- The __ClassLoader__ subsystem is responsible for this.


2. __Verifying__
	- Ensures the byte code follows Java's security rules and doesn't perform unsafe operations
	- Prevents malicious or corrupted code from running


3. __Executing__
	- Converts byte code into machine code using a Just-In-Time (JIT) compiler or an interpreter and executes it.
	


4. __Memory management__
	- Manages memory through __heap__ and __stack__
	- Includes automatic __Garbage collection__ to reclaim memory used by objects no longer in use.
	


5. __Thread management__
	- Manages threads in a multi threaded Java program