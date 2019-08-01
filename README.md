# NodeScheme
This project is still in the trial phase.

The current existing Scheme to JavaScript is mostly an interpreter implemented on the JavaScript running-time. In the web environment, there is extra running-time overhead and extra download overhead (to download the interpreter code).

The goal of this project is to compile the Scheme code into readable JavaScript code with no additional runnig-time overhead and avoid the download overhead.

The generated code should be readable and free to use on both the browser and server side. The code that runs should use the garbage collector and stack space of the JavaScript running-time. It will be free to call the JavaScript library, seamlessly integrate with [Schism](https://github.com/google/schism) (the generated JavaScript code works with the generated [WASM](https://webassembly.org) binary code), work with [React](https://reactjs.org) / [React Native](https://facebook.github.io/react-native/) / JSX, and run efficiently on [Node.js](https://nodejs.org/).

The goal of the project is to compile a subset of Scheme into ES6 Javascript, which is designed to be applied to dynamic types, web programming with macros. The current goal is to support syntax-rules, call/cc, and automatic tail recursion optimization.

In the future, efforts will be made to extend to the Scheme standard and support the syntax-case.

NodeScheme running on [Chez Scheme](https://www.scheme.com) to compile the Scheme code into JavaScript code and use the [Nanopass](http://nanopass.org) framework to design the compiler backend.
