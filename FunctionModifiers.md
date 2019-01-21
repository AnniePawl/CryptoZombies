# Function Modifiers
A modifier allows you to control the behavior of your smart contract functions.</br>There are different types including: **view functions** and **pure functions**

### View functions
Similar to constant in that it *does not change any state values of the contract.* </br>
Tells compiler that storage data won't be written as a result of the function call, so no network verification required.</br>
No transaction to mine --> No gas to spend
```
function _generateRandomDna(string _str) private view returns (uint) {
}
```

### Pure Functions
Function data is either passed in or defined in it's scope. </br>
In Solidity, pure funcs aren't allowed to even read(let alone write) storage data.


# Return Values
The function declaration contains the type of the return value.</br>
Here's how to return a value from a function: </br>
```
string greeting = "What's up dog";

function sayHello() public returns (string) {
  return greeting;
}
```
