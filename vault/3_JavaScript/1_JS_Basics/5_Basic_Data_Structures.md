# 5. Basic Data Structures
Created Thursday 09 July 2020

## Array
- Array is dynamic.
- Syntax

```js
let list = [1, "two" , [3,4] ]; // mixing and nesting is OK
```

- Arrays are objects, and are assigned as references.
- Array may be pooled. However, this doesn't affect the code.
- Array API

| Action                        | Code                                             | Return Value     | Comment                                                                                           |
|:----------------------------- |:------------------------------------------------ |:---------------- |:------------------------------------------------------------------------------------------------- |
| Access Element                | A[0], or A.at(0) (supports negative indexes)     | element          | Same as C++                                                                                       |
| Get length                    | A.length                                         | length(number)   | This property is readable/writable: it can change array size.                                     |
| Check if element in array     | `A.includes(x)`                                  | Boolean          |                                                                                                   |
| Append                        | A.push(newVal)                                   | new length       |                                                                                                   |
| Remove tail                   | A.pop()                                          | removed element  | returns removed element. Error if array is empty.                                                 |
| splice(changes memory)        | A.splice(goal_index, \#deletions, val1, val2...) | deleted array    | Delete \#deletion elements and add val1, val2 etc at goal index(inclusive).                       |
| Remove at index               | A.splice(destination_index, 1)                   | element          | Removes ith element                                                                               |
| Remove head                   | A.splice(0, 1)                                   | element          |                                                                                                   |
| Resize Array                  | A.length = new_length;                           | length(number)   |                                                                                                   |
| slice(extract subarray)       | A.slice(start, length=A.length)                  | extracted array  | No change in array, just like substr in C++                                                       |
| Clear(current reference only) | A = []                                           | void             | No change at memory location.                                                                     |
| Deep copy                     | `structuredClone(A)`                             | array            | Shipped to browsers 2022                                                                          |
| Fake deep copy (change shell) | B = \[...A]                                      |                  | New memory allocated, same behavior for array literal rvalue.                                     |
| reverse array                 | A.reverse()                                      |                  | Inplace and reference as return value.                                                            |
| Expand/Decrease array size    | A.length = new_length                            |                  | Change is in-place.                                                                               |
| Linear Search                 | A.indexOf(key)                                   | number (integer) | Returns -1 if key not found. Returns leftmost key index (if duplicates).                          |
| Reverse Linear Search         | A.lastIndexOf(key)                               | Extended ops     |                                                                                                   |
| sort                          | A.sort(criteriaFunction=LexCompare)              | sorted array     | function (a, b) { return numericDifference}; Return negative (swap yes), 0 or positive (no swap). |
| join array of strings         | A.join(sep='')                                   | string           |                                                                                                   |

- Array can have empty values. Workaround: `Array(10).fill(null)`
- The [spread operator](4._Advanced_Arrays.md) is indispensible. It is used almost everywhere.

## Object
- Objects - It is a set of key-value pairs.
- `Object` is a keyword.
- Syntax:
```js
var user = {
  name: "John",
  age:34,
  hobby: "Socccer",
  isMarried: false, // , does not matter
  shout: function(){ console.log(this.name);}, // method, can use 'this'.
  };

  user.favoriteFood = "spinach"; // add a member to an object
  user['favoriteFood'] = "spinach"; // same as above
```
- `undefined` - unitialized value, or accessed non-existent key in object. Example: 
	```js
	const x = { name: 'Alice' }; // x['Bob']
	```
- `null` - Represents the state of being empty(consider like a null pointer). `null` and {}(empty object) are different.
- Properties can be accessed by `objectA.property_name` or `objectA[property_name]`.
- Check key membership - `x.hasOwnProperty('fieldName')`
- `this` is not accessible if the method is run after isolation.
- Objects are not index sub-scriptable. Unless the key used is deliberately a number.


## String
- `string` is a primitive type.
- Strings are dynamically sized, immutable in JS.
- String API - no in-place ops.

| Action                     | Code                           | Return Value     | Comment                                                             |
|:-------------------------- |:------------------------------ |:---------------- |:------------------------------------------------------------------- |
| Access Element             | s.charAt(index)                | string           | [] works too. But fails for edge cases - 'hello'\[true] is an error |
| string exists within       | `s.includes(x)`                | Boolean          |                                                                     |
| Get length                 | s.length                       | length(number)   | This property is readable/writable: it can change array size.       |
| Concatenation              | a+b                            | string           | Works with non-string                                               |
| Char --> ASCII number      | s.charCodeAt(index)            | number           |                                                                     |
| ASCII --> character        | String.fromCharCode(65)        | string           | Need to use String class                                            |
| Substring                  | s.substr(start, len=A.length)  | removed element  | start, length based extraction                                      |
| Slice                      | s.slice(start, end=end)        | extracted array  | \[start, end) based extraction                                      |
| UpperCase                  | s.toLocaleUpperCase(lang='en') |                  | same as toUpperCase() for EN. Similar syntax for lowercase.         |
| Reverse string             | s.split(`).reverse().join(`)   |                  | Inplace and reference as return value.                              |
| Expand/Decrease array size | A.length = new_length          |                  | Change is in-place.                                                 |
|                            |                                |                  |                                                                     |
|                            |                                | Extended ops     |                                                                     |
| Prefix membership          | s.startsWith(key_string)       | boolean          | Same as Python3                                                     |
| Suffic membership          | s.endsWith                     | boolean          | Same as Python3                                                     |
| Split                      | s.spit(delim=undefined)        | array of strings | No splitting without delimiter                                      |
| Trim whitespace            | s.trim()                       | array            | No arguments. trimLeft, trimRight are available.                    |


## Resources:
- [TIme Complexity of popular ops](https://dev.to/lukocastillo/time-complexity-big-0-for-javascript-array-methods-and-examples-mlg)
