[[Integer type]] (`byte`, `short`, `int`, and `long`)
	- [[byte type]]
	- [[short type]]
	- [[Integer type]]
	- [[long type]]

[[Floating-point type]] (`float` and `double`)
- [[Floating-point type]]
- [[double type]]

[[String]]



- When evaluating an expression with values of mixed types, Java automatically converts the operands to appropriate types.

- You can explicitly convert a value from one type to another using the `(type)value` notation.

- Casting a variable of a type with a small range to a type with a larger range is known as widening a type.

- Casting a variable of a type with a large range to a type with a smaller range is known as narrowing a type.

- Widening a type can be performed automatically without explicit casting. Narrowing a type must be done explicitly. 

| Data type | Size    | Range                                                   | Example use case                 |
| --------- | ------- | ------------------------------------------------------- | -------------------------------- |
| `byte`    | 1 byte  | -128 to 127                                             | Memory-critical systems          |
| `short`   | 2 bytes | -32.768 to 32.767                                       | Large arrays of small numbers    |
| `int`     | 4 bytes | -2.147.483.648 to 2.147.483.647                         | General-purpose calculations     |
| `long`    | 8 bytes | -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 | Space science, big data, finance |

