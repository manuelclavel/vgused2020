# Introduction

## Teaching methods of the module ##
>> Lectures: interactive lectures
>> Exercises: Teamwork in small groups

- Small teams of 3 students. Randomly generated.

## Prerequisites for module participation ##
>> Prerequisites: passing of all attestations parallel to
>> the unit ``Exercise-Software Engineering-Desing''

- Git private repository for each team

- ***Action point*** Team ledears send <full name, VGU id, Github name>
for each member of the team.

## Type and form of assessment:
### Lecture
>> Written exam 90 minutes 
- Individual exercise.
### Exercise
> Prerequisite: attestation during the exercises

## Grading of the assessment
### Lecture
>> Differentiated
### Exercise
- Undifferentiated

## Contents of the unit
-   Software design process
-   Software design **principles**
-   Software design **concepts**
-   Software **architecture**
-   **Object-oriented** software design
-   System design process
-   Software design with **patterns**
-   Software Testing

# Day 1: Lecture
- Notes originally created by Mr. Pankaj Jalote,
Indian Institute of Technology Delhi, as supporting material for
his book: "A Concise Introduction to Software Engineering".

 
## Software Design 

- Design activity begins with a set of requirements, and maybe an architecture
- Design done before the system is implemented
- Design focuses on **module view** – i.e. what modules should be in the system
- Module view may have easy or complex relationship with the **C&C view**
- Design of a system is a blue print for implementation
- Often has two levels – **high level** (modules are defined), 
and **detailed design** (logic specified)

## Design 

- Design is a creative activity
- Goal: to create a plan to satisfy requirements
- Perhaps the most critical activity during system development
- Design determines the major characteristics of a system
- Has great impact on testing and maintenance
- Design document forms reference for later phases
- Design methodology – systematic approach for creating a design

## Design Concepts 
- Design is **correct**, if it will satisfy all the requirements 
and is consistent with architecture
- Of the correct designs, we want best design
- We focus on **modularity** as the main criteria (besides correctness)

## Modularity 
- Modular system – in which modules can be built separately 
and changes in one have minimum impact on others
- Modularity supports independence of models
- Modularity enhances design clarity, eases implementation
- Reduces cost of testing, debugging and  maintenance
- Cannot simply chop a program into modules to get modularly
- Need some criteria for decomposition – 
**coupling** and **cohesion** are such criteria

## Coupling
- __Independent modules__: if one can function completely without the presence 
of other
- Independence between modules is desirable
  - Modules can be modified separately
  - Can be implemented and tested separately
  - Programming cost decreases
- In a system all modules cannot be independent
- Modules must cooperate with each other
- More connections between modules
  - More dependent they are
  - More knowledge about one module is required to understand the other module.
- Coupling captures the notion of dependence

## Coupling...
- Coupling between modules is the strength of interconnections between modules
- In general, the more we must know about module A in order to understand module B  the more closely connected is A to B
  - __Highly coupled__ modules are joined by strong interconnection
  - __Loosely coupled__ modules have weak interconnections

## Coupling...
- Goal: modules as loosely coupled as possible
- Where possible, have independent modules
- Coupling is decided during high level design
- Cannot be reduced during implementation
- Coupling is inter-module concept
- Major factors influencing coupling
  - Type of connection between modules. Complexity of the interface
  - Type of information flow between modules

## Coupling - Type of connection
- Complexity and obscurity of interfaces increase coupling
- Minimize the number of interfaces per module
- Minimize the complexity of each interface
- Coupling is minimized if
  - Only defined entry of a module is used by others
  - Information is passed exclusively through parameters
- Coupling increases if
  - Indirect and obscure interface are used
  - Internals of a module are directly used
  - Shared variables employed for communication

## Coupling - interface complexity
- Coupling increases with complexity of interfaces: 
eg. number and complexity of parms
- Interfaces are needed to support required communication
- Often more than needed is used eg. passing entire record 
when only a field is needed
- Keep the interface of a module as simple as possible

## Coupling - Type of info flow
- Coupling depends on type of information flow
- Two kinds of information: data or control.
- Transfer of control information
  - Action of module depends on the information
  -  Makes modules more difficult to understand
- Transfer of data information
  - Module can be treated as input-output function
- Lowest coupling: interfaces with only data communication
- Highest: hybrid interfaces

## Cohesion
- Coupling characterized the inter-module bond
- Reduced by minimizing relationship between elts of different modules
- Another method of achieving this is by maximizing relationship between elts of same module
- Cohesion considers this relationship
- Interested in determining how closely the elements of a module are related to each other
- In practice both are used

## Cohesion ...
- Cohesion of a module represents how tightly bound are the elements 
of the module 
- Gives a handle about whether the different elements of a module belong together
- High cohesion is the goal
- Cohesion and coupling are interrelated
- Greater cohesion of modules, lower coupling between module
- Correlation is not perfect.

## Levels of Cohesion
- There are many levels of cohesion.
  - Coincidental
  - Logical
  - Temporal
  - Communicational
  - Sequential
  - Functional
- Coincidental is lowest, functional is highest
- Scale is not linear
- Functional is considered very strong

## Determing Cohesion
- Describe the purpose of a module in a sentence
- Perform the following tests

  -  If the sentence has to be a compound sentence, 
contains more than one verbs, the module is probably performing 
more than one function. 
Probably has __sequential__ or __communicational__ cohesion.

  - If the sentence contains words relating to time, 
like "first", "next", "after", "start" etc., the module probably 
has __sequential__ or __temporal__ cohesion.

  - If the predicate of the sentence does not contain a single specific object 
following the verb, the module is probably __logically cohesive__. 
Eg "edit all data", while "edit source data" may have functional cohesion.

  -  Words like "initialize", "clean-up" often imply __temporal cohesion__.

- Functionally cohesive module can always be described by a simple statement

## Summary
- Goal of designing is to find the best possible **correct** design
- **Modularity** is the criteria for deciding **quality** of the design
- Modularity **enhanced by low coupling and high cohesion**.

