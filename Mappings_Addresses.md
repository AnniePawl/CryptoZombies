# Mappings and Addresses
Make a multi-player game by giving zombies in our database an owner. </br>
**Two datatypes are needed:**</br>
- Mapping
- Addresses

## Addresses
**An address is owned by a specific user or smart contract**</br>
Ethereum blockchain is made of _accounts_,
    - Accounts have **addresses**, which are like bank accounts numbers (unique identifier)
    - Accounts have a balance of **Ether**, which can be sent and received from other accounts.

## Mappings
Mappings are another way of storing organized data in Solidity!
A mapping is essentially a key-value store storing and looking up data.


This is how you define a mappings:</br>
In 1st example, key= an address, value= a unit</br>
In 2nd example, key= a unit, value= a string.  
```
// For a financial app, storing a uint that holds the user's account balance:
mapping (address => uint) public accountBalance;
// Or could be used to store / lookup usernames based on userId
mapping (uint => string) userIdToName;
```
