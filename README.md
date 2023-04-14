# TypeScript
This repository contains the concepts of TypeScript.

<br>

- TypeScript is a superset of JavaScript.
- It does not provide any new feature compared to javaScript.
- It just allows us to write our code in a more precise way such that it reduces the number of errors at the runtime.
- Its all about "Type Safety".
- It's a development tool.Our code still runs in JS.
- The TS code gets complied to JS.

## What TypeScript does?
 ``` Static Checking ```
- It analyze our code as we type.

Say if I'm adding 2+"2" in JS, then it give us '22' as a result 👇
But that's not correct we can't add a number to a string or to a null value or to undefined. And this is where TS comes into picture, it analyze our code while we write and whenever we are performing any operations between variables of different types it makes squiggly lines to indicate that we are performing a wrong operation & may get an error.
It also makes sure that we aren't using a variable/object/function that aren't defined, if we do so then it shows us squiggly lines.

<img src ="https://user-images.githubusercontent.com/75883328/231961685-78a83567-a98c-4f72-b1ac-cd47813c40c1.png" height=300px width = 800px />


