# 77-777's Haskell - The Manual

> Pragmatic information about Functional Programming and Haskell.

<br>
<br>

DRAFT.

Work in progress.

<br>
<br>

## Audience

Click the sections below to expand.

<br>
<br>

<details>
  <summary> For Intermediate Programmers </summary>

---

### Spawning a project & building

* Ecosystem & Environment
  * ? - primary build and project manager
  * Cabal - package manager
  * todo.
  * GHC - the Glasgow Haskell Compiler. 

Please use your respective *nix package manager.

`sudo apt-get install ghc`


<br>
<br>
<br>

### Console Arguments & Printing

```haskell
  
```

### File IO

```haskell
  
```

### Directory & File Operations

```haskell
  
```

### Data Type Conversion

```haskell
  
```

### String Handling

```haskell
  
```

### Threading & Process Handling

```haskell
  
```

### Sockets

```haskell
  
```

### GUI

```haskell
  
```

### Web Requests

```haskell
  
```

### Web Framework

```haskell
Yesod
```

### Web Automation

```haskell

```

### Data Structures

```haskell

```

### Logging
```haskell

```

### Config Storage

### Regex & Levenshtein
  
### Cryptography

### Parsing HTML/JSON/XML

### Error Handling & Exceptions

### Timers, Events, Promises



### Database Access / ORM
  
### Graphics

### Keywords in Haskell

```haskell

-- Packages & Modules --
import, module, where, instance, deriving

-- Imperative & Unit IO
do, ()

as
-- Variable scope --
let .. in

-- Data & Objects
data, type, class

-- Control Flow & Guards/Pattern Matching --
if, else, then, forall, case, 

-- Others --
default
hiding
proc

-- Types & Options --

Char, Bool, Int, Integer, Double

```

### Symbols in Haskell

* State Symbols

```haskell

```

* Structure Symbols

``haskell
   
```

* Operator Symbols

``haskell

```

<br>
<br>

</details>

<details>
  <summary> For Beginner Programmers </summary>

---

### Types & Records

```haskell
data Vehicle = Vehicle Integer String Double
  
data Vehicle = Vehicle {
  year_release :: Int,
  make :: String,
  speed :: Double
}
  
let my_vehicle = Vehicle { year_release = 2020, make = "Mitsubishi", speed = 20.0 }
```

### Modules

```haskell
import BoxMod


module Car
  where
  
  getSpeed :: Int
  getSpeed = 5
  
  
module Computation (
  addNum,
  subNum
) where
  
  addNum :: Int -> Int -> Int
  addNum x y = x + y
  
  subNum :: Int -> Int -> Int
  subNum x y = x - y
  
  generateValue :: IO
  generateValue = do
    side_effect_call
  
  isTrue = do
    if 1 == 1 then
      True
    else
      False
```

### Functions

```haskell

increment y = y + 1
  
  
getIntValue x
  | x == "5" = 5
  | y == "7" = 7

  
isOneHundred :: Integer -> Bool
isOneHundred a
  | a == 100 = True
  | _ == _ = False

  
addNumbers :: Integer -> Integer -> Integer
addNumbers a b = a + b


getConstant :: Double -> Integer
getConstant 0.0 = 0
getConstant 1.0 = 1


switcher :: String -> String
switcher x | x == "Hi" = "Hello"
switcher y | y == "Bye" = "Gooodbye
  
main :: IO
main = do
  increment 5
  addNumbers 3 2
```

### Polymorphism

```haskell

```

### Variables

```haskell

```

### If Statements

```haskell

```

### Looping & Control Flow

```haskell
  
```

### Recursion & List Manipulation/Patterns

```haskell
  
```

### Interfaces (Typeclasses)

```haskell

```

### Generics & Constructor Parametrization

```haskell

```

### Functors

<br>
<br>

</details>

<details>
  <summary> For Expert Programmers </summary>

---

### FFI

The foreign function interface for interoping with native code and the os.

### DLLs / Shared Libraries

Accessing functions directly from shared libraries.

### Compiler/Interpreter Tweaks

Optimization, compiling or interpreting, linking, bytecode generation, garbage collection, etc.

### Project Layout & Code Structure

1 module file can contain multiple nested submodules. 
Scaffolding/ers.

### Architecture

Patterns. Functors and Monads.

### Good Practice

Clarity. Avoid surprises. DRY principle. SOLID principle if using OOP.

<br>
<br>

</details>

<details>
  <summary> For Functional Programming Dummies </summary>

---

### Terminology

* Purity
  * Functions that produce no side effects. Given an input, the ouput should be the same on said input no matter what the state of the system is. If this rule is broken, the function is not pure.

* State
  * Commonly used to refer to structures, variables, code or the system which can change at any moment in time. Code changing in other places other than their grouped scope is considered bad practice.

* Side Effect
  * When a function emits the notion of modyfing state outside of it's scope such as globals or dependencies.

* Unit/IO Notation
  * Commonly known/referred as the "void" type, (), this notation is used to indicate that a function will do or "return" an IO side effect operation that changes some system/program state.

* Expression
  * Also called compute/computation, is any calculation or subexpression that MUST return a value as a result. In the functional mindset, a program is a series of expressions and subexpressions but ultimately going down to a single value outputted. ("Figure of speech")

* Immutability
  * Data created/assigned with values at spawn time which cannot be changed afterwards. Can be predicted since it is constant.

* Mutable Data
  * Data that can be affected by side effects/IO.

* Records
  * Groups of types aligned together under a single type. It is the "structure/struct" aspect of functional programming.

* First Class Citizen
  * Any entity that can be treated as you treat a variable, which means you can add it to another, compute it, pass it as an argument to another function and/or return it as a value.

* Functions as First Class Citizens
  * Functional paradigm prides itself on the notion that some (depends on language) functions are ultimately variables, can be declared as such, can be passed as arguments and can be returned. This is the notion of function pointers for those who know C. Commonly used for callbacks, events and other procedural code.

* Higher Order Functions
  * Functions that are treated as First Class Citizens. Basically function pointers. In Haskell, not all functions are higher order functions.

* Function Composition
  * Calling functions which rely on values returned by calling another function. E.g. f(g(x)).

* Arity
  * The number of parameters a function has. Lengthy parameters for a function (e.g high Arity) smells of a badly coded function or a complex one.

* Currying
  * Complex functions which have a high arity need to be broken down. This simplification process is called currying.

* Functors
  * Factory pattern kin.

* Lambda Calculus
  * Anonymous function spawning notation.

* Polymorphism
  * The act of having and passing data that holds multiple "forms". A stream object for example might be a base entity for a filestream, networkstream, pipestream or whatever.

* Generics
  * Having data structures that can be reused with other types. Particularly lists. Lists of integers or bytes or strings as an example.

* Meta Programming
  * Programs written that generate other programs/code.

* Dependency Injection
  * A concept used to manage portability and hotswap, as common usecases. One implementation of dependency injection is the IoC container for dependency inversion.

* Typeclasses
  * Haskell's "interfaces" to modules.

* Monads
  * 

* Zippers
  * 

### Functional Paradigm Aims

* Functional Application
  * Functional programming is all about having pure functions and calling those pure functions to transform your data. Everything is an expression and your IO should be separated and organized in a high level fashion.

* Functional Purity
  * Functions without side effects that are agnostic of system state. As many as you can. Why? Said functions are easy to test, well design and don't depend on external factors. (in theory)

* IO & Side Effect Separation
  * A tremendous amount of errors, bugs and malpractice happens as a result of poor state management. Having a more organized flow where IO is separate from pure code provides clarity to where errors may occur as well as visual guidance to where program logic/computation is located.

* Reduce state and constrain/isolate it
  * Removing for, while loops is one way to reduce state and instead do things recursively.

* Low Function Arity Through Currying


* Simple & Flexible Data Transformation
* Low Coupling, High Cohesion
* Type Correctness
* Immutability unless otherwise altered
* Recursivity
* Declaratively define problems
* Write less, Do more
* Lower bug rate

<br>
<br>

</details>

<br>

<details>
   <summary>External Dependencies</summary>

---

### Common Libraries

Cabal is the official Haskell package manager.

`cabal install <pkg-name>`

| Library  | Purpose | Comments |
| -------- | ------- | ----- |
| | | |

<br>
<br>

</details>

<details>
   <summary>A Better Standard API Reference</summary>

---

## The Standard API

Click each module to expand and see their exposed functions and types.

```haskell
(* Importable Modules *)



(* Console, File IO, Etc *)



(* Date, Time, Math *)


(* Related to Types *)


(* Data Structure Modules *)


(* Algorithms. Hashing, RNG, Sort, Etc. *)


(* Concurrency, Parallelism, Synchronization *)


```

</details>
  
<br>
