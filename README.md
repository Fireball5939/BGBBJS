# A Beginner's Guide to BitBurner and JavaScript
Welcome to my guide on BitBurner where we go from zero knowledge on JavaScript (Or TypeScript, if you so choose) to a fully fledged script to hack the best server!

### What you need
* Obviously, you'll need access to BitBurner. It can be found on [Steam](https://store.steampowered.com/app/1812820/Bitburner/) or on the internet as two seperate builds. [Main (stable)](https://bitburner-official.github.io/) or [Dev](https://bitburner-official.github.io/bitburner-src/)
* Yes, that's it!

# Table Of Contents
* [JavaScript](#javascript)
* [Advanced](#advanced)
  * [TypeScript](#typescript)

# JavaScript
Now, if we covered all of JavaScript then this would be a web development course, not a guide on BitBurner. As such, we'll be focusing on the basic concepts that you'll need to understand everything that ***you*** create to make a fully functional hacking script. Or at least to cover everything (Along with the downsides) that the game's given basic-hack-template script has. (Almost) All lines in JavaScript should end in a semicolon (;), The exception to this is anything with Curly braces ({ }).

## Variables
In JavaScript, there's 4 major parts to every variable
* Declaring
* Assigning
* Scope
* Types
### Declaring
Declaring a variable is the actual process of *creating* it, until a variable is declared using one of the 3 key words (`const`, `let`, `var`) it can't be used. When a variable is declared it is *initialized* (Initially created) with the value `undefined` (More on `undefined` in [Types](#types))
* Const.
 Immutable, cannot be changed after declaration. Intended for things you know you will use throughout the code but won't ever be changed. Conforms to [Block Scope](#block-scope).
* Let.
 Mutable, can be changed after declaration. Intended for defaulting to one value then changing it later depending on a condition or if a variable in general needs updating. Conforms to [Block Scope](#block-scope).
* Var.
 Mutable, can be changed after declaration. DEPRECATED AND SHOULD NOT BE USED, but will still be shown in this section for the reason of knowing how older code works. Mostly the same as `let`. Conforms to [Function Scope](#function-scope).
```js
const x; // This is invalid syntax, more on this later.
```
```js
let x;
```
```js
var x;
```
### Assigning
Assigning a variable is what actually gives/changes a variable's data. This is done by putting an equals sign (=) after the variable's name, then after the equals sign sets the value of the variable to that.
```js
const x = "Hello World!";
```
Note: Although `let` and `var` can be split as shown below `const` variables MUST be in one line
```js
let x;
x = "Hello World!";
```
```js
var x;
x = "Hello World!";
```
Something almost everyone does is combine the declaration and assignment into a single line, like is done with `const`.
### Scope
In JavaScript (As well as most other languages, I understand) one thing you have to worry about with variables is scope. If you've ever seen a permission/social status/heierarchy pyramid it's a lot like those (But reversed). The scope level of a variable is determined by where it is defined... TBC
# NOTE
This guide is incomplete, I am trying to get this finished within a reasonable amount of time (aka before I jump ship and get bored with this). Current focus is finishing Scope, and doing a quick explanation for Types (Will be focused on in the TS Migration portion) in [Variables](#variables), after that I will focus on [Functions](#functions)
