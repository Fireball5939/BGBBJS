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
JavaScript is, at its core, ~~an object oriented language~~ a language where every type is technically an object. If you've ever seen a JSON file (Which stands for JavaScript Object Notation btw) or the syntax for JSON then you'll know what actual *objects* are like in JavaScript.
### Variable Types
In JavaScript there are many different Types. Each type has its quirk, and in all honesty in types aren't all that important with BitBurner JavaScript. If you choose to later migrate to [TypeScript](#typescript) then types are very important (I wonder where the name comes from) and WILL throw errors if incorrect types are used.
#### Null
#### Undefined
#### Boolean
#### Number
#### BigInt
#### String
#### Symbol

### Defining Variables
In JavaScript there's ~~2~~ 3 different ways to *define* variables. When you define a variable you are essentially taking a particular section of memory and saying "You! Remember that you are containing this data!" so that you can use it at a later time.
#### Const
Const, the vanilla of variable defining. Bland, Boring, and Basic. You define the variable, and that is it. For any data type not resulting from some formula with a changing result, no different than spamming the same boolean or string in place of the variable.
```js
const constant = `Hello World!`;

```
