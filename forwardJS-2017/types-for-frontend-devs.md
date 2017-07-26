# Types for Frontend Developers

## Different types of javascript typed libraries
- Typescript
- Flow
- Elm

Dynamically typed - type checked at runtime

Statically typed - types checked at compile time

Type Inference - typescript has this feature

let myVar: boolean
is the same as
let myVar = true

Javascript DOES has types, they are just not static types

## Benefits To Using Types

1) Precision - benefits of static typing… allows us to be precise with what we are saying with our code

Strings are the worst. Strings shouldn’t be used for data if possible

2) Enforce Invariance -  helps us know what will break at compile time. If we provide a string but expect a number things will break
 type myType = string | number
3) Shapes - Define the shape of our data
const fullName = (obj: Person) : string => { return ${obj.fname} + ${obj.lname} } (TypeScript)
the above takes in a person and returns a string

4) Reduce number of tests we have to write

5) Increase confidence - Increases our understanding of code and increases our confidence that our code does what we expect

Tooling

Static types help make tooling better

## Trade Offs
- Unfamiliarity
- Verbosity - increases how verbose your code is. More code has to be written
- Extra build step
- Definition files
- Interop
- ANY - dont let typescript infer any to avoid this proble

## Why should ANY be avoided?
- Undos what we’ve built with static typing.
