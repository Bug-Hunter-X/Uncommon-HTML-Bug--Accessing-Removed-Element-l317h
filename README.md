# Uncommon HTML Bug: Accessing Removed Element

This repository demonstrates a subtle bug in JavaScript that can occur when manipulating DOM elements. The core issue lies in trying to access and modify the properties of a DOM element after it has been removed from the page (or is effectively removed by setting its display to 'none').

## The Bug
The provided `bug.html` file contains a `div` element that's initially visible. A button triggers a JavaScript function that clears the div's content, hides it using `style.display = "none"`, and then attempts to change its background color.  This will lead to an error or unexpected behavior.

## The Solution
The `solution.html` file presents a corrected version. Instead of trying to modify the element after it's removed, we check if the element still exists and only then apply the style changes.  This avoids the error entirely.

## How to Reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Click the button.  You'll likely observe a JavaScript error in your browser's console.
4. Repeat steps 2 and 3 with `solution.html` to see the corrected behavior.

## Lessons Learned
This example highlights the importance of careful DOM manipulation.  Always validate that elements exist before attempting to access or modify their properties, especially after operations that might remove them or change their visibility.