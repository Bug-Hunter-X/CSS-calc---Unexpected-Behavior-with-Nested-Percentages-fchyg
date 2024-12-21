# CSS calc() Unexpected Behavior with Nested Percentages

This repository demonstrates an uncommon issue with the CSS `calc()` function when using percentages within nested calculations.  The problem arises when attempting to subtract a fixed value (e.g., pixels) from a percentage-based width within a nested element. The expected behavior is not always observed.

## Bug Description

The `calc()` function doesn't always correctly calculate the percentage based on the parent element's width in nested scenarios.  Instead, it might use a different reference point, often the viewport's width, resulting in incorrect dimensions.

## How to Reproduce

1. Clone this repository.
2. Open `bug.css` and `bugSolution.css` to see the problematic and corrected CSS respectively.
3. Observe the difference in the rendering of the `.inner` element.

## Solution

The solution provided in `bugSolution.css` involves using `vw` (viewport width units)  to explicitly base the calculation on the viewport's width, thereby achieving the intended result.

## Note

This issue is less common and highlights the importance of understanding the context in which `calc()` operates, especially with percentages in nested elements.