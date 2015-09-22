Lecture One
===========
Course materials: http://github.com/barak/mu-cs424-f2015
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
Cobol
-----
* understandable-to-naive-reader syntax

FORTRAN
-------
= Formula Translator
(subprograms = procedures and functions)
````fortran
	y = a+(b*c)-(d*e)
````
Lisp
----
* reified λ calculus
* s-expression as datatype

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
