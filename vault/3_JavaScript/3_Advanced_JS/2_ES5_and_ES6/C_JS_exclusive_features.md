# C. JS exclusive features
Created Thursday 25 March 2021

#### 1. Symbol data type
- Useful when working with objects.
- Used to create properties in objects which are invisible to the object owner.
- This is important if different people work on the same object. Separation of concerns is the goal, symbols avoid properties to clash, if the object is handled by two scripts.
- There is a global symbol registry, syntax, Symbol.for('id') is used to get the key for id, this is useful if we want some symbols to be the same in a team where a project has many teams.
- Symbol() don't auto-convert to strings, which is why obj[id1] is different for different people.

      id = Symbol('id'); // desciption does not affect the hash value
      const obj = {
      	[id]: 23;
      }

      // we can add our own properties to an existing object
      id1 = Symbol();
      obj[id1] = 231; // not accessible to the original user even if he uses property name as id1

  FIXME
#### 2. use `strict`
- Purpose - Modern mode for JS, generates more exceptions that usual. It can be enforced at the **function** or **script** level. [See](https://johnresig.com/blog/ecmascript-5-strict-mode-json-and-more/).
- Syntax - add `"use strict"` at the first line inside the function, class or script. Only comments may appear about the `"use script"`.
- It is just a signal for the interpreter.
- Gotcha - There's no way to "cancel" `"use strict"`, once enabled.
- Example
	```js
	// Example 1 - Globally
	"use strict"; // for the whole script
	
	///_ code_/
	
	// Example 2 - Selective
	function f()
	{
		"use strict"; // for the function
		// code
	}
	function g()
	{
		/_code_/ // no effect of "strict"
	}
	```

- Is it used often? There are two cases:
  - Code using classes and modules - Not required. `"use strict"` is enabled inside these by default.
  - Old codebases - `"use strict"` is encouraged.