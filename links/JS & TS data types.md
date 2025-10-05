- **Primitives**
  - Number (1, 2, 3, 10, 3.14)
  - String ("Hello", 'world')
  - Boolean (true, false)
  - Undefined (let x;) No value inside the variable.
  - Null (let x = null;) An empty value inside of the variable
  - Symbol (const id = Symbol('id');) Unique string.
  - BigInt (the huge numbers like 12345678901234567890n)
- **Objects types**
  - Object (key: "value" collection { name: "John", age: 30 })
  - Array ([1, 2, 3, "a", "b", "c"])
  - Function ( function greet() { return "Hello"; } )
- Etc (**Map, Set, Date**)

TS datatypes:
- **Any**. Disables type checking `let x: any = 42;`
- **unknown**. Safer alternative to **`any`**. Requires explicit type checking before use:
	`let value: unknown;`
	`if (typeof value === "string") {`
	  `value.toUpperCase(); // OK`
	`}`
- **void**: For functions that return nothing
- **never**: For functions that never complete or always throw an error
	`function throwError(): never {`
	  `throw new Error("Error");`
	`}`
- **Union Types**: Union of types. `let value: string | number = "hello"; value = 42;`
	`interface Props {`
	  `value: string | number;`
	`}`
- **Intersection Types**: Combination of a few types
	`interface A { name: string; }`
	`interface B { age: number; }`
	`type C = A & B; // { name: string, age: number }`
- Enums
	`enum Status {`
	  `Pending = "PENDING",`
	  `Success = "SUCCESS",`
	  `Error = "ERROR",`
	`}`
	`let state: Status = Status.Success; // "SUCCESS"`
- Generics: Universal types for flexibility:
	`function getArray<T>(items: T[]): T[] {`
	  `return items;`
	`}`
	`const numbers: number[] = getArray([1, 2, 3]);`
	***
	`interface ListProps<T> {`
	  `items: T[];`
	  `renderItem: (item: T) => JSX.Element;`
	`}`

