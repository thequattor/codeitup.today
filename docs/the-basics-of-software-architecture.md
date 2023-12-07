---
sidebar_position: 1
---

# The basics of software architecture

Software Architecture defines fundamental organization of a system and more simply defines a structured solution. 
It defines how components of a software system are assembled, their relationship and communication between them.

## Software architecture

* Meets all the requirements
* Performance optimized
* Security in check
* Manageability for developers
* Scalability for business growth
* Accessibility for easier user experience

## Major requirements for project

* User requirements – the way end-users interact with the system
* Business requirements – cheaper, faster, better than competitors
* IT system requirements – infrastructure requirements

## Two types of requirements

* Functional - Business flows, What the user should do, User interfaces
* Non-functional - Performance, Load, Data volume, Concurrent users, SLA


## Architecture abstraction

* Layers - System, Sub-systems, Layers, Components, Classes, Data and Methods
* Bad Architecture - Complex, Incoherent, Brittle, Untestable, Unmaintainable 
* Good Architecture - Simple, Understandable, Flexible, Testable, Maintainable

## Key principles

* Separation of concerns: Each object and module should be in its own concern and context
* Single responsibility principle: Elements in our design must have a single purpose
* Principle of least knowledge: Components do not know about the internals of other components, Done through interfaces
* Don’t repeat yourself: Don't have multiple components with the same purpose
* Minimize upfront design: Try to design the minimum architecture so that developers can work

## Layer Guidelines

* Separate areas of concern: Each layer should have one role only
* Define communication between layers: How does the presentation layer communicate with the business layer? 
* Use abstraction to loosely couple layers: Use interfaces for every communication, Objects should not be tight to a particular platform or technology
* Don’t mix different types of components in a layer 
* Use a consistent data format within a layer

## Component Guidelines

* No component should rely on the internals of another: Components should be black boxes
* Do not mix roles in a single components: Web controllers should not have business logic, Business layer should not have HTTP concerns 
* Define clear contracts for components: All public methods and properties should be scoped in advance
* Abstract system wide components away from other layers: As soon you have a component which is accessible in multiple layers, Put it in a system-wide area of concern
