Lecture One
===========
Course materials: http://github.com/barak/mu-cs424-f2015

Introduction
------------
What are programming languages?
People invented computers wtihout the need for programming languages. People inputted instructions via patch panels. Next evolution of computing came with Program Storage Computers.

Charles Babbage designed first computer however even with the resources at his disposal, his design was far too complex to implement. Ada Lovelace was known as a contributor to Babbages work.

Just before WW2, the first Electronic Computer was invented by Conrad Zuessy.
Also invented the one of the earliest programming languages which contained floating-point arithmetic among it's features -> Called 'Zwei Program'

Efforts in Benchley Park were all done manually (See Alan Turing/Enigma machine). No programming language existed.

Assembly
--------

````assembly
;; calculate a+(b*c)-(d*e)
	load d
	mul e
	store t
        load b
	mul c
	add a
	sub t
````
The first big leap in programming. Uses a symbolic language to translate to machine code.
Big pain point with Assembly is that writing formulas can easily become difficult.

Cobol
-----
* understandable-to-naive-reader syntax
* [Admiral Grace Hopper](https://en.wikipedia.org/wiki/Grace_Hopper) is credited for developing the first iteration of the COBOL language as well as its compiler.
* Very similar to FORTRAN stylistically
* Very natural syntax 
````cobol
	ADD 7
	TO 9
	YIELD B
````

FORTRAN
-------
= Formula Translator
(subprograms = procedures and functions)
````fortran
	y = a+(b*c)-(d*e)
````

A growing idea at the time was the use of Natural Languages to describe a *formula* and have a component that *transcribes* what was written to Machine Code.
The result of this was a famous language called *FORTRAN*. (Formula - Translator)

This language alleviates the pressure of allocating memory. It exists at a very close level to Assembly in terms of architecture. 

FORTRAN was designed with the following in mind:
* Low level details hidden
* Handles storage allocation (including array indexing)
* Treated the machine the program was designed for as a basic RAM machine
* Very close to a Turing Machine

Lisp
----
* reified λ calculus
* s-expression as datatype - (Represents reusable segments of code. See [here](https://en.wikipedia.org/wiki/S-expression) for more info)

Algol
-----
* block structure
````algol
   if zero(x) then begin print something; do something; end else begin ... end
````
* was non-eager evaluation (instead call-by-need) (Algol68)
* like Haskell (sorta: Haskell is "lazy")

Prolog
------
* Prolog = Logic Programming
* resolution theorem proving
* Formal systems -> produce theorems -> ask questions.
* Japanese threw a load of money into Prolog.
* Look around for '5th Generation Computing Project'

Strings and Search
------------------
* SNOBOL
* Icon

Object Oriented
---------------
* SIMULA67
* Smalltalk80
* Oaklisp (scheme + objects)
* Java

Tower of Power
==============
* lazy evaluation
* first-class functions
* monads
* purity
* algebraic data types
* logic variables, unification, and resolution theorem proving (ala Prolog)

Each language has a different level of expression when it comes to certain problems. All of the languages are Turing-equivalent when it comes to pure computation, but one thing might be better expressed in one language than another.

Once you have learned more programming languages then some problems become much easier to solve.

One expressive example would be an infinite list. Imagine a function that produces a list of approximations but the accuracy of these approximations increases as you tend to infinity. When generating this list with the likes of a for loop, you would have to pass in some ɛ-accuracy to the loop, like termination and progression. Extra allocations that can be avoided generally. Also on that, the original caller has to be aware of this ɛ-accuracy. This can cascade very easily in a hierarchy of callers (Modularity Issue).

Infinite lists are very easy to implement in lazily evaluated languages which is very good for modularity in numeric code.

Some other nice features include:

* First class functions
* Can be used for concise expression.
* Monads (Not enough time in lecture to explain)
* Purity (See [here](https://en.wikipedia.org/wiki/Pure_(programming_language)) for an in-depth look into purity in programming languages)
* Some programming languages can be considered 'Pure' (Mathematically pure)
* Pure functions have no side-effects
* Pure functions will never alter any state on the machine, thus guaranteeing that a function will produce the same output for the same input
* Very good at parallelization
* Pure functions cannot interfere with each other



