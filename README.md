# Uncommon HTML Bug: Accessing Non-Existent Element

This repository demonstrates a subtle bug that can occur in HTML when attempting to access a DOM element that doesn't exist using `document.getElementById()`. This can lead to unexpected behavior or silent failures, making it difficult to debug.

The `bug.html` file contains the erroneous code.  The `bugSolution.html` file shows the corrected version.

## Bug Description

The bug arises from an attempt to modify the `innerHTML` property of an element that has not been created or is not present in the DOM.  This results in a runtime error, potentially preventing the rest of your JavaScript from executing. 

## Solution

Always ensure that the element you're targeting with `document.getElementById()` actually exists in the HTML before attempting to manipulate it.  Use checks (e.g., `if (element)` or `try...catch`) to handle cases where the element is not found.