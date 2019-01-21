## Typecasting
Important for converting between data types.

## Hash Functions
A hash function maps an input into a random 256-bit hexadecimal number. </br>
Slight input change results in big hash change.

## Keccak256
A **built-in hash function**
**Hash Functions** </br>
Helpful for generating semi-random uint (secure random number generation is a difficult challenge in blockchain) </br>
Expects a single parameter of type bytes (required to "pack" any parameters before calling keccak256).</br>
**Example**</br>
The return values below are totally different, despite only a 1 character change in the input.
```
//6e91ec6b618bb462a4a6ee5aa2cb0e9cf30f7a052bb467b0ba58b8748c00d2e5
keccak256(abi.encodePacked("aaaab"));

//b1f078126895a1424524de5321b339ab00408010b7cf0e6ed451514981e58aa9
keccak256(abi.encodePacked("aaaac"));

```
