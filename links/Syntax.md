`let  age: number = 33;`
`let name: string = "Vetol";`
`let isActive: boolean = true;`
`let numbers: number[] = [1, 2, 3]; Only numbers!`
`let strings: string[] = ["a", "b", "c"]; Only strings!`

`let mixed: (number | string)[] = [1, 2, 3];` 
`mixed.push("hello"); // OK`
`mixed.push(4); // OK` 
`mixed.push(true); // ERROR: boolean it is not the number OR the string`

