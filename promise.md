# promise

- https://www.codecademy.com/courses/asynchronous-javascript/lessons/promises/exercises/constructing-promises
- The Promise constructor method takes a function parameter called the **executor function** which runs automatically when the constructor is called. The executor function generally starts an asynchronous operation and dictates how the promise should be settled
- The executor function has **two function parameters**, usually referred to as the resolve() and reject() functions. The resolve() and reject() functions aren’t defined by the programmer. When the Promise constructor runs, JavaScript will pass its own resolve() and reject() functions into the executor function:
  - resolve is a function with one argument. Under the hood, if invoked, resolve() will **change the promise’s status from pending to fulfilled**, and the **promise’s resolved value will be set to the argument passed into resolve()**.
  - reject is a function that takes a reason or error as an argument. Under the hood, if invoked, reject() will change the promise’s status from pending to rejected, and the promise’s rejection reason will be set to the argument passed into reject().
