# 4. Using JS
Created Wednesday 08 July 2020

## In the browser
- Using the `<script>` `</script>` tag.

There are 2 ways to add JS code:
1. Add it as content of the `script` tag.
	```html
	<!-- Method 1, direct -->
	<body>
	<script> var x = 2; </script>
	<body>
	```
2. Add code from a `.js` file using `src` attribute. `script` is still a content tag.
	```html
	<!-- Method 2, src -->
	<body>
	<script src="path"></script> <!-- Leave tag content empty -->
	<body>
	```

Note:
- Keep the `script` tag at the end of the `body` tag, and never in the head. Reason: Executing/downloading `script` content blocks the rendering process. *Or*, add the `defer` attribute to the `script` tag, place it anywhere now.

## In the terminal
- Write code in `.js` files.
- Run them using `node file.js` in a terminal.

#### REPL
- Start the REPL using `node` command.

#### Differences
- In the browser, you may use objects like `window`, but this is an error in the terminal.
- UI APIs like `document` are also absent.