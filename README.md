# CSS Blur Issue with Fixed Position Elements

This repository demonstrates a subtle bug related to the CSS `filter: blur()` property when applied to an element with `position: fixed;`.  The expected behavior is that the blur should affect the underlying elements.  However, due to how fixed positioning works, the blur is often confined to the fixed element only.

The `bug.css` file contains the problematic code, while `solution.css` provides a workaround to achieve the desired effect.

## How to reproduce:
1. Clone this repository.
2. Open `index.html` (which you'll need to create - it should contain elements demonstrating the problem). 
3. Observe how the blur only affects the fixed element and not the elements behind it.

## Solution:
The solution typically involves creating a pseudo-element (`::before` or `::after`) on a parent element, applying the blur to that pseudo-element, and positioning it strategically to cover the affected area.  See `solution.css` for an implementation.