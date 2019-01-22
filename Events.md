# Events
Events provide a way for a contract to communicate to an application's front-end that something happened on the blockchain. Your app's front-end can *listen* for certain events and take action when they happen.

### Event Declaration Example
```
event IntegersAdded(uint x, uint y, uint result);

function add(uint _x, uint _y) public {
  uint result = _x + _y;
  // fire an event to let the app know the function was called:
  emit IntegersAdded(_x, _y, result);
  return result;
}

```

### Event Listener Example
```
YourContract.IntegersAdded(function(error, result) {
  // do something with result
}

```

### New Zombie Event example
*NewZombie* event should pass *zombieID*(uint), *name*(string), and *dna*(uint)

```
event NewZombie(uint zombieId, string name, uint dna);

```
