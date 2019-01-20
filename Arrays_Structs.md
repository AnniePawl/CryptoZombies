## Structs
Structs allow us to create more complicated data types that have multiple properties.

**Zombie Struct Example**
```
struct Zombie {
    uint dna;
    string name;
}
```

## Arrays
Arrays are helpful when you want a collection of something</br>
There are two types in Solidity:
- **fixedArray**
- **dynamicArray**

Array with a fixed length of 2 elements:
`uint[2] fixedArray;`</br>
Another fixed Array, can contain 5 strings:
`string[5] stringArray;`</br>
Dynamic Array, has no fixed size, can keep growing:
`uint[] dynamicArray;`

### Array of Structs
A dynamic array of structs is useful for storing structured data in your contract (like a db)</br>
`Person[] people;`

### Public Arrays
Arrays can be declared as public, and Solidity will automatically create a "getter" method for it.
`Person[] public people;`

## Working with Structs and Arrays
Here's how to create new zombies and add them to Array
```
Zombie zoob = Zombie(172,"Zoob");

zombies.push(zoob);
```
This can also be written as one line of `zombies.push(Zombie(172, "Zoob"))`
