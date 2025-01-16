# TypeScript Type Error Not Caught at Compile Time

This repository demonstrates a scenario where a TypeScript type error is not caught during compilation, only surfacing at runtime. This is due to the limitations of TypeScript's type inference in certain complex or dynamic scenarios.

The bug showcases an example where passing a string to a function that expects a number does not trigger a compile-time error. The error only becomes apparent at runtime when the function attempts to perform addition on a string and number.

## How to Reproduce

1. Clone this repository.
2. Compile the code using `tsc bug.ts`.
3. Run the compiled JavaScript code.

You'll observe that the code compiles without errors, but during execution, the runtime exhibits unexpected behavior (string concatenation).

## Solution

The `bugSolution.ts` file demonstrates a strategy to mitigate this issue. In this case, a runtime check helps prevent unexpected concatenation.  Other options include more robust type guards and input validation.