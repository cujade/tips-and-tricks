# JAVASCRIPT (WEDNESDAY)
- runs on client-side
- enables interactivity
- console.log
- jQuery - a library (set of resources to make doing certain things easier)
	- "write less, do more"
	- in the case of jQuery, it makes **almost everything** easier
		- HTML document traversal/manipulation
		- event handling
		- animation
- JS variables
	- dynamically type
	- value type not strongly enforced - variable represents a value of any type
		- number, string, object, etc.
- JS arrays
	- 0-indexed
	- indexing
	- iteration
	- var fruits=["apple", "banana"]
		fruits.length
		fruits[n]
		fruits.forEach(function(item, index, array))
			console.log(item)
- jQuery
	- $ - alias for JQuery
	- e.g. jQuery selectors
		- $('p') -> document.getAllElementsByTagName('p')
		- $('#id') -> document.getElementById('id')
		- $('.class') -> document.getElementByClass('class')
- similar to google fonts, jQuery downloaded from cdn - content delivery network
- event handling
	- instead of inline onclick, we can specify `on` event
- safest way to execute JS/jQuery
	- $(document).ready(function() {}
	- or, `document.addEventListener('DOMContentLoaded', function_name, false);`
- callback functions
	- code that runs after animation finishes
	- executed inside another function
		- function passed to another function

## TODO
- talk about process
	- jsfiddle
	- browsersync
		- browser-sync start --server --files "css/*.css"
	- sublime plugins
		- ColorHighlighter 
- sublime tips
	- folder/sidebar
	- tabbing/shift-tabbing
	- ctrl+l - select a line
	- ctrl+a - select everything
	- ctrl+d - select word, repeat to select more
	- edit+sortlines - sort lines (css)
	
