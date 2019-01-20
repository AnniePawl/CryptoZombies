# State Variables & Integers
**State Variables** are permanently stored in contract storage, meaning they are written to Ethereum blockchain (Think of them like writing to a DB)

### Example
```
contract Example {
    //this will be stored permanently in blockchain
    uint myUnsignedInteger = 100;
}
```

## Unsigned Integers: uint
**uint** is an alias for **uint256** </br>
**uint** data type is an *unsigned integer*, meaning its value must be *non-negative*</br>
There is also an **int** datatype for *signed integers*
