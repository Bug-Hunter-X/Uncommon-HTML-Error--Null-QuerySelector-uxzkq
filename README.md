# Uncommon HTML Bug: Null QuerySelector

This repository demonstrates a subtle yet common error in HTML JavaScript interaction: attempting to modify the innerHTML of an element that might not exist using querySelector.  This can easily happen if selectors are not perfectly accurate or if dynamic content changes the DOM structure.  The provided `bug.html` shows the problematic code, while `bugSolution.html` provides a solution.

## Bug
The bug is present within the JavaScript code of `bug.html`. It attempts to directly manipulate the innerHTML of an element returned by `document.querySelector`. If that selector fails to find the element (returns `null`), this action results in a runtime error.

## Solution
The `bugSolution.html` file demonstrates a robust approach. Before modifying the element, it checks if the querySelector returned a valid element. This avoids the error by handling the `null` case gracefully.