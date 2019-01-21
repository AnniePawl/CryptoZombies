## Public Functions
Public functions = **default** in Solidity.</br> This means anyone can call on contract's function and execute its code. This can make it vulnerable to attacks...

## Private Functions
**Better to mark as private!**</br>
This means only other functions within our contract will be able to call this function and add to array

### Private Function Example
```
Zombie[] public zombies;

 function _createZombie(string _name, uint _dna) private {
     zombies.push(Zombie(_name, _dna));
 }
```
