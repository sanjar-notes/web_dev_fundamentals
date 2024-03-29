# 1. DOM and JS Engine
Created Saturday 11 July 2020

## The DOM (Document Object Model)
We assumed, until now that HTML is _just_ rendered by the browser. Now, before rendering, there needs to be some concrete representation of the HTML in memory. This representation is called the **Document Object Model**(DOM). It is created by the browser as soon as the HTML is received.

- It is simply a tree structure (document) that represents the skeleton(structure) of the webpage.
- If we can edit the document, we can effectively change the whole page.
- Strictlys speaking, it has got nothing to do with CSS or JS, even if they are present. Small [caveat](https://bitsofco.de/what-exactly-is-the-dom/) regarding JS though.

![](../../../assets/1_DOM_and_JS_Engine-image-1-a09ebfc7.png)
**The HTML DOM is a standard for how to get, change, add, or delete HTML elements.**

---

- The whole page is stored(in memory) as an object named **document**
- It does not look like an object because Chrome recognized it's a special object, but it is still a JS object.
	![](../../../assets/1_DOM_and_JS_Engine-image-2-a09ebfc7.png)

```js
document.write('Hello'); // document the write method
```

**Think of the **document** object as the skeleton of the screen that we see(with our eyes).**
Note: DOM and document are used interchangeably.
[DOM vs CSS vs reality](https://bitsofco.de/what-exactly-is-the-dom/#:~:text=This%20is%20because%20the%20DOM,styles%20applied%20to%20the%20element.)


## The JS Engine
- We assumed that JS is just loaded and run in the browser, but how?
- Every browser has an interpreter to run JS code.
- Some popular ones (and apps using them) are
  1.  V8 - Chrome and Node.js
  2.  ChakraCore - IE and Microsoft Edge
  3.  SpiderMonkey - Firefox and other stuff. GNOME3 shell.
  4.  Nitros - Safari
- These engines execute the JavaScript line by line.

## `window` and `document` objects
- The document has a parent object called the `window` - represents the current tab.
- The `window` object also has the `alert()`, `prompt()` functions including the `document` object itself.
	![](../../../assets/1_DOM_and_JS_Engine-image-3-a09ebfc7.png)
- `window` is the default object if unspecified, i.e f() ↔ window.f()

Note: window cannot be written to for UI stuff usually, because it is just the action part.
```js
window.write(  '<p>abcd</p>'); // error
document.write('<p>abcd</p>'); // Okay
```