# 4. Function composition
Created Thursday 25 March 2021

TODO

#### What is Composition
- Writing functions where the input of the outer function is the output of the inner function, and this is true for all. Implementing f(g(h(x))) using main_func(f, g)(arg).

#### Syntax
```js
const g = (foo) => (/*code*/); // takes function as argument
const h = (a) => (/*code*/); // takes value as argument

const f(g, h) = (x) => f(g(x)); // composition definition

f(g(x)); // call
```
- Accumulation of context is optional.

#### Why do this
- For concise code
	```js
	// Without composition
	function f(g, h)
	{
	
	}
	
	// With currying
	let add => x => y => z => (x + y + z);
	let a1 = add(1)(2);
	let a2 = add(10)(20); //
	
	// calling is the same
	```
- Currying vs Composition - Currying is a multi-argument system and composition is multi-function(not multi-purpose) system.
