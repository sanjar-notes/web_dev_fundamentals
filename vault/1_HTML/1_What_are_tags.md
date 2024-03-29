# 1. What are tags
Created Sunday 14 February 2021

### What is HTML
- It is a language used to specify the structure(skeleton) of a webpage.
- HTML is a markup language, not a programming language.
- HTML stands for HyperText Markup Language

### Tags
- The basic unit of HTML is the tag.
- There are two kinds of tags
  1.  Content tags(or just tags). Example: `<p> HTML is genius </p>`
  2.  Self closing(or empty tags). Example: `<img />`

### Attributes
- An attribute is a key-value pair that modifies the behavior of a tag.
- They are written inside the opening angled brackets.
- Syntax:
  ```html
  <img height="200px" width="200px" />
  ```
- Parts of an attribute:
  1.  key - a string without quotes.
  2.  value

* `=` is used for assigning values to key.

- Rules for attributes:
  - Attributes are separated by space.
  - Ordering of attributes does not matter.
- Presence of a boolean attribute means it is enabled.

  ```html
  <video autoplay="true" />
  <!-- verbose -->

  <video autoplay />
  <!-- concise is better -->
  ```

### Anatomy of a webpage
- There are 3 basic tags in all webpages.
  1.  `html` - encloses the whole webpage.
  2.  `head` - contains title(tab title) and page metadata. Used by crawlers.
  3.  `body` - webpage content, as seen in the browser.
- Basic structure of a webpage.

```html
<!DOCTYPE html>
<!--Ignore this for now-->
<html>
  <head> </head>

  <body></body>
</html>
```

- Everything inside the `body` is visible(perceptible) in the browser(below the omnibox).
- The preamble, `<!DOCTYPE html>` is used for legacy reasons. It's not a part of the webpage and just describes the file type.

### Other basic tags
- `title` - appears on the tab. Page file name is displayed if this is absent. Used within `head`.
- `meta` - self closing tag specifying metadata like language, region, character encoding etc.

### Facts about HTML
- Errors are ignored by the browser. [See](https://youtu.be/-csXdj4WVwA)(optional).
- Whitespace is ignored in the content of HTML tags, except in string literals.
- HTML does not have strict indentation, it is free flow language.
