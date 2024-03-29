# 2. Map, filter and reduce
Created Thursday 25 March 2021

## Why use map, filter or reduce?
- Map, filter and reduce help us to make our code functionally pure(deterministic).

## 1. Map
- Purpose - store f(ele) for each element, in a **map object**.
- Syntax - `arr.map(f)`; where f can be a function in any form.
- Assume an argument when defining f.
- f(ele) is computed and stored for each element. `undefined` is stored if `f` returns nothing.
- The map object is index subscriptable.

![](../../../../assets/2_Map,_filter_and_reduce-image-1-4ce68a0b.png)

## 2. Filter
- Purpose - returns an iterable of elements for which f(ele) is true.
- Syntax - same as map.

![](../../../../assets/2_Map,_filter_and_reduce-image-2-4ce68a0b.png)

## 3. Reduce
- Purpose - Accumulates the result by running f(accum,ele) for each element.
- Syntax - `arr.reduce(f, accum_start=0)`
- You must have _accumulator_ and _element_ as parameters of `f`, in order.

```js
const arr = [1, 2, 3]
const res = arr.reduce(((accum, ele)=> accum + ele), accum_init_value); // 0 if unspecified
// same as doing accum = accum + ele each time
```

- Remember to update accum inside f().

Note:
- All the quick for functions - **forEach**, **map**, **filter** and **reduce** work sequentially by default. They can be made parallel, however.
- Iteration number is available all **forEach**, **map** and **filter **- as the second parameter of `f`. This is optional.

## Gotchas
- `map` and `filter` return an array as output, while `reduce` returns a single value (usually).
- Use these anytime we need loops for small things.
- forEach is different, it returns nothing.
