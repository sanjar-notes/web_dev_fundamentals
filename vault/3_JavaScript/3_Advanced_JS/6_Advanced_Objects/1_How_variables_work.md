# 1. How variables work
Created Thursday 25 March 2021

FIXME

#### Reference types
All the datatypes except the primitive ones(number, boolean, string, null, undefined, symbol). e.g Array, Set, Object etc.

- Reference types are compared(=== and ==) only by their address, no bit by bit comparison is performed.
- All data-structures(except strings) are reference types. This is the reason [] and [] is false, they are actually two empty arrays stored at two locations.
- Shallow copy is done for all reference type assignments.

![](../../../../assets/1_How_variables_work-image-1-7ed442d7.png)
![](../../../../assets/1_How_variables_work-image-2-7ed442d7.png)

- Why is it so? - This makes code efficient, and comparing big types doesn't make sense.
- All primitive types are passed by value, and all the others are passed by reference.
