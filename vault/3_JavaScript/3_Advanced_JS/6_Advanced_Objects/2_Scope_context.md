# 2. Scope context
Created Thursday 25 March 2021

**Context** - The parent object, or answer to the question'What parent object environment are we in ?'

* Accessed using the **this** keyword
* When we run f(), it is equivalent to this.f(), i.e run w.r.t the parent object.
* A simpler definition - What's on the left side of the dot. e.g alert('Hello') has window as it's context because it is equivalent to window.alert('hello');
```js
function f()	// context of f is the same as LOC sibling to f
{
	const a = 10;	// a does not affect the parent - 'this' talks about parent object.
	return this;
}
console.log(this===f()); // -> true for a webpage, this and f() reference the document
```


* How to change context - we need to be inside another object.
	![](../../../../assets/2_Scope_context-image-1-7ed442d7.png)
Note that lambda function doesn't acknowledge a change in parent object but a function does.

FIXME: <https://youtu.be/zE9iro4r918> ``this`` keyword, ``apply`` and ``bind``

