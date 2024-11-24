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
 Should NEVER be used unless you know exactly what you're doing and why. Many people will instantly correct your usage of `var` to `let` when you ask for help. Mutable like `let` is, and conforms to [Function Scope](#function-scope). It's such bad practice to use, unless you know what you're doing, that `var` will not be covered for the rest of this guide. DO NOT USE!!!
```js
const x; // This is invalid syntax, more on this in the next section.
```
```js
let x;
```
### Assigning
Assigning a variable is what actually gives/changes a variable's data. This is done by putting an equals sign (=) after the variable's name, then after the equals sign sets the value of the variable to that.
```js
const x = "Hello World!";
```
Note: Although `let` can be split as shown below `const` variables MUST be in one line
```js
let x;
x = "Hello World!";
```
Something almost everyone does is combine the declaration and assignment into a single line, like is done with `const`.
### Scope
In JavaScript, as well as most languages, such a thing exists called Scope. This referrs to where things that are declared can and can't be used, and is usually defined as each set of `{ }` being a "block." Code inside of a block can use any variables, classes, functions, and so on which are declared in a higher block or in the current block, given it has been created. However anything in lower blocks cannot be accessed from a block higher than that.

Perhaps this is slightly confusing, here's an example of scope.
```js
export async function main() {
 const msg = "Hello World!";
 if (msg === "Hello World!") {
  let foo = 1;
  console.log(foo); // Prints 1 to the console
  console.log(msg); // Prints the string "Hello World!" to the console.
 }
 console.log(msg); // Prints the string again to the console
 foo = 2; // Throws an error saying foo is undefined, this is because foo is in a lower block scope than here and cannot be accessed from here.
 console.log(foo); // Code is never reached, but if it was run it would throw an error because of foo being undefined
}
```
What we first do is we define a new variable, msg, and initialize it with the value `"Hello World!"` This is a `const` variable and cannot be changed later, if we attempted to reassign a value to it (Such as `msg = "I've been changed..."`) it would throw an error. Then we check to see if the value of `msg` is equal to `"Hello World!"`, which it is. This runs the code inside of the pair of curly braces, which is a new block level.
Inside of this new block level, we declare the variable `foo` and initialize it with a value of `1`. After that we print the value of `foo` to the console, then print the value of `msg` to the console. Now we have exited the scope of the if function and the variable `foo` disappears. We print the value of `msg` to the console again, and then we try to assign a value of `2` to the variable `foo`. Because `foo` has in essence disappeared an error is thrown saying that `foo` is undefined, because it literally is not in the scope.
## If statements
If statements are an extremely powerful, versetile, and useful tool in every programming language. They allow you to not just carry out a set of instructions, but add logic to your code.
