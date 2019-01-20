## Zombie DNA
- Each zombie has a unique, random appearance
- Appearance based on "Zombie DNA" (16-digit integer)
- Different parts of number refer to different traits
    - First 2 digits = zombie head type, etc
        - If first 2 digits of our example DNA above are 83. To map that to the zombie's head type, we do 83 % 7 + 1 = 7. So this Zombie would have the 7th zombie head type.

## Zombie Factory
- Maintains database of zombies in army
- Has a function for creating new zombies
