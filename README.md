# Multiple Event Listeners on Same Element in HTML

This repository demonstrates an uncommon bug in HTML related to attaching multiple event listeners to the same element using different methods.  The bug occurs when `onclick` and `addEventListener` are used simultaneously, potentially causing unexpected behavior and performance issues.

## Description
The `bug.html` file shows the erroneous code where an event listener is set using both the `onclick` property and the `addEventListener` method for the same event type ('click'). This redundant setup can lead to multiple executions of the event handler.

The `bugSolution.html` demonstrates the corrected code where only `addEventListener` is used to cleanly and efficiently manage event handlers.

## How to reproduce
1. Clone this repository.
2. Open `bug.html` in a web browser.
3. Click the div element. You'll notice the alert message appears twice, illustrating the unexpected execution.
4. Now open `bugSolution.html`, click the div, and see the alert message only appears once.

## Solution
Always use the standard `addEventListener` method for attaching event listeners. It's more flexible, allows you to attach multiple listeners for the same event, and avoids potential conflicts or unexpected behaviors compared to using the `onclick` property directly.