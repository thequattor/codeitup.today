---
sidebar_position: 2
---

# The basics of S.O.L.I.D

In software engineering, SOLID is a mnemonic acronym for five design principles intended to make object-oriented designs more understandable, 
flexible, and maintainable. 

The principles are a subset of many principles promoted by American software engineer and instructor Robert C. Martin first introduced 
in his 2000 paper Design Principles and Design Patterns discussing software rot.

## The SOLID idea

* The Single-responsibility principle: "There should never be more than one reason for a class to change." In other words, every class should have only one responsibility.
* The Open–closed principle: "Software entities ... should be open for extension, but closed for modification."
* The Liskov substitution principle: "Functions that use pointers or references to base classes must be able to use objects of derived classes without knowing it."
* The Interface segregation principle: "Clients should not be forced to depend upon interfaces that they do not use."
* The Dependency inversion principle: "Depend upon abstractions, [not] concretions."

## Single-responsibility principle

"A class should have only one reason to change".
Because of confusion around the word "reason" he has also clarified saying that the "principle is about people."
In some of his talks, he also argues that the principle is, in particular, about roles or actors. 
For example, while they might be the same person, the role of an accountant is different from a database administrator. 
Hence, each module should be responsible for each role.

## Open–closed principle

In object-oriented programming, the open–closed principle (OCP) states "software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification".
that is, such an entity can allow its behaviour to be extended without modifying its source code.

The name open–closed principle has been used in two ways. Both ways use generalizations (for instance, inheritance or delegate functions) to resolve the apparent dilemma, but the goals, techniques, and results are different.

Open–closed principle is one of the five SOLID principles of object-oriented design.

## Liskov substitution principle

Liskov's notion of a behavioural subtype defines a notion of substitutability for objects; that is, 
if S is a subtype of T, then objects of type T in a program may be replaced with objects of type S without altering any of the desirable properties of that program (e.g. correctness).

Behavioural subtyping is a stronger notion than typical subtyping of functions defined in type theory, 
which relies only on the contravariance of parameter types and covariance of the return type. Behavioural subtyping is undecidable in general: 
if q is the property "method for x always terminates", 
then it is impossible for a program (e.g. a compiler) to verify that it holds true for some subtype S of T, even if q does hold for T. Nonetheless,
the principle is useful in reasoning about the design of class hierarchies.

Liskov substitution principle imposes some standard requirements on signatures that 
have been adopted in newer object-oriented programming languages 
(usually at the level of classes rather than types; see nominal vs. structural subtyping for the distinction):

* Contravariance of method parameter types in the subtype.
* Covariance of method return types in the subtype.
* New exceptions cannot be thrown by the methods in the subtype, except if they are subtypes of exceptions thrown by the methods of the supertype.

In addition to the signature requirements, the subtype must meet a number of behavioural conditions. These are detailed in a terminology resembling that of design by contract methodology, leading to some restrictions on how contracts can interact with inheritance:

* Preconditions cannot be strengthened in the subtype.
* Postconditions cannot be weakened in the subtype.
* Invariant cannot be weakened in the subtype.

## Interface segregation principle

Within object-oriented design, interfaces provide layers of abstraction that simplify code and create a barrier preventing coupling to dependencies. 
A system may become so coupled at multiple levels that it is no longer possible to make a change in one place without necessitating many additional changes.
Using an interface or an abstract class can prevent this side effect.

## Dependency inversion principle

In object-oriented design, the dependency inversion principle is a specific methodology for loosely coupled software modules. When following this principle, the conventional dependency relationships established from high-level, policy-setting modules to low-level, dependency modules are reversed, thus rendering high-level modules independent of the low-level module implementation details. The principle states:

* High-level modules should not import anything from low-level modules. Both should depend on abstractions (e.g., interfaces).
* Abstractions should not depend on details. Details (concrete implementations) should depend on abstractions.

By dictating that both high-level and low-level objects must depend on the same abstraction, this design principle inverts the way some people may think about object-oriented programming.

The idea behind points A and B of this principle is that when designing the interaction between a high-level module and a low-level one, the interaction should be thought of as an abstract interaction between them. This not only has implications on the design of the high-level module, but also on the low-level one: the low-level one should be designed with the interaction in mind and it may be necessary to change its usage interface.

In many cases, thinking about the interaction in itself as an abstract concept allows the coupling of the components to be reduced without introducing additional coding patterns, allowing only a lighter and less implementation-dependent interaction schema.

When the discovered abstract interaction schema(s) between two modules is/are generic and generalization makes sense, this design principle also leads to the following dependency inversion coding pattern.
