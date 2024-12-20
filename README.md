# Accessing HTML element before it is fully loaded

This repository demonstrates a common yet subtle error in HTML: attempting to access and manipulate a DOM element before it has fully loaded. This can lead to unexpected behavior or errors, such as `null` or `undefined` when trying to access the element's properties.

## The Bug

The `bug.html` file contains a script that tries to hide a div element (`#myDiv`) immediately after it is defined. This can cause issues if the script runs before the browser has fully parsed and rendered the HTML.

## The Solution

The `bugSolution.html` file demonstrates the correct approach by using the DOMContentLoaded event listener to ensure the script only runs after the entire HTML document is fully parsed and the DOM is ready. This prevents errors and guarantees that the element exists before the script manipulates it.