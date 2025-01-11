# Uncommon HTML Bug: Removing Element with innerHTML=null

This repository demonstrates an uncommon bug in HTML where setting the `innerHTML` property of an element to `null` unexpectedly removes the element from the DOM instead of simply clearing its content.  This is a subtle error that can be easily missed.

## Bug Description
The bug occurs when using `innerHTML = null` to clear the content of an HTML element.  Intuitively, one would expect only the content within the element to be removed, leaving the element itself intact. However, setting `innerHTML` to `null` completely removes the element from the document's structure.

## Solution
To clear the content of an element without removing it, use either `innerHTML = ''` (empty string) or `textContent = ''`.  These methods effectively remove the content, but preserve the element in the DOM.

## How to reproduce the bug
1. Open `bug.html` in a web browser.
2. Click the 'Click Me' button.
3. Observe that the div element with the id "myDiv" is removed from the page.

## How to view the solution
1. Open `bugSolution.html` in a web browser.
2. Click the 'Click Me' button.
3. Observe that the div element with the id "myDiv" is still present, only its contents are cleared.