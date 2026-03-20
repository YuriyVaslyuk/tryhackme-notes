# JavaScript Essentials - TryHackMe Notes

## What is JavaScript
JS is a scripting language that runs directly in the browser on the client side.
Because it runs on the user's machine, anyone can access and mess with it.
That's what makes it the main attack surface for web hacking.

## Variables
Three ways to declare variables: var, let, const.

- var is the old way. It leaks outside the block it was created in so it can
  be accessed or changed from places it was never meant to be touched. Security risk.
- let is the modern way. Block-scoped, it stays where it belongs.
- const is the same as let but the value is locked once set. Can't be reassigned.

## Functions
A function is a reusable block of code you give a name to. Instead of writing
the same logic over and over, you write it once and just call it whenever you need it.

## console.log
Same as print() in Python. Outputs to the browser console.
Developers sometimes forget to remove console.log statements before pushing to
production, and end up logging sensitive stuff like tokens or user data.
Checking the browser console is one of the first things you do when poking at a web app.

## Security Takeaway
Because JS runs client-side, anyone can open the browser console (Ctrl+Shift+I in Chrome)
and run their own JS on any page. That's the whole idea behind XSS attacks ---
you inject malicious JS into a page and the victim's browser runs it without knowing.
