## Typecasting
Important for converting between data types.

## Hash Functions
A hash function maps an input into a random 256-bit hexadecimal number. </br>
Slight input change results in big hash change.

## Keccak256
A **built-in hash function**</br>
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

### Generate Random DNA Example
**Line 1:** takes keccak256 hash of abi.encode... to generate a pseudo-random hexadecimal</br>
Typecasts it as a uint </br>
Finally stores result in a uint called rand. </br>
**Line 2:** returns value modulus dnaModulus b/c we want DNA to be 16 digits long.

```
function _generateRandomDna(string _str) private view returns (uint) {
     uint rand = uint(keccak256(abi.encodePacked(_str)));
     return rand % dnaModulus;
 }

```
