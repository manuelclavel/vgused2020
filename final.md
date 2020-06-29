# Final Day

# Review content
## Day 1
- Goal of designing is to find the best possible correct design  
- Modularity is the criteria for deciding quality of the design
- Modularity enhanced by low coupling and high cohesion.

## Day 2
- Design patterns

## Design patterns
### Creational design patterns
- These design patterns are all about class instantiation.
  - The new operator considered harmful.
#### Factory Method (Day 2)

#### Prototype (Day 3)
- Specify the kinds of objects to create using a prototypical instance, 
and create new objects by copying this prototype.
- Co-opt one instance of a class for use as a breeder of all 
future instances.

#### Abstract factory (Day 4, day 5)
- Provide an interface for creating families of related 
or dependent objects without specifying their concrete classes.

- Map out a matrix of "platforms" [= sport centers] 
versus "products" [events/resources - bookings].

- Often, designs start out using Factory Method (less complicated) 
and evolve  toward Abstract Factory, Prototype, or Builder 
(more flexible, more complex) 
as the designer discovers where more flexibility is needed.

#### Singleton (Day 5)
- Ensure a class has only one instance, 
and provide a global point of access to it.

- [extra point] Encapsulated "just-in-time initialization" 
or "initialization on first use".

### Structural Design Patterns
- Ease the design by identifying a simple way to realize 
relationships between entities.

#### Adapter (Day 6)
- Convert the interface of a class into another interface clients expect. 
- Adapter lets classes work together that couldn't otherwise because of 
incompatible interfaces.
- Wrap an existing class with a new interface.

#### Facade (Day 7)
- Provide a unified interface to a set of interfaces in a subsystem.

- Facade defines a higher-level interface that makes the subsystem 
easier to use.

- Wrap a complicated subsystem with a simpler interface.

- The client uses (is coupled to) the Facade only.

- If the Facade is the only access point for the subsystem, 
it will limit the features and flexibility that "power users" may need.

#### Proxy (Day 8 -- homework)

#### Decorator (Day 8)

- Attach additional responsibilities to an object dynamically. 
Decorators provide a flexible alternative to subclassing 
for extending functionality.

- Client-specified embellishment of a core object by recursively wrapping it.

- Wrapping a gift, putting it in a box, and wrapping the box.

- Ensure the context is: a single core (or non-optional) component,
  several optional embellishments or wrappers, and an interface that
  is common to all.
  
-  The client is always interested in CoreFunctionality.doThis(). The
   client may, or may not, be interested in OptionalOne.doThis() and
   OptionalTwo.doThis(). Each of these classes always delegate to the
   Decorator base class, and that class always delegates to the
   contained "wrappee" object.

- Adapter provides a different interface to its subject.  Proxy
provides the same interface.  Decorator provides an enhanced
interface.

- Decorator and Proxy have different purposes but similar
  structures. Both describe how to provide a level of indirection to
  another object, and the implementations keep a reference to the
  object to which they forward requests.

#### Composite (Day 9)
- Composites that contain Components, each of which could be a Composite.

#### Iterator (Day 10)
- Provide a way to access the elements of an aggregate object 
sequentially without exposing its underlying representation.

#### Visitor (Day 11)
- Represent an operation to be performed on the elements of an object
structure.

- Visitor lets you define a new operation without changing the classes
of the elements on which it operates.


#### Observer (Day 12)

- Define a one-to-many dependency between objects so that when one
  object changes state, all its dependents are notified
  and updated automatically.

- Encapsulate the core (or common or engine) components in a Subject
  abstraction and the variable (or optional or user
  interface) components in an Observer hierarchy.

- The "View" [what to do when something change] part of Model-View-Controller.

#### Mediator (Day 13)

- Define an object that encapsulates how a set of objects
  interact. Mediator promotes loose coupling by keeping objects from
  referring to each other explicitly, and it lets you vary their
  interaction independently.

- Design an intermediary to decouple many peers.

- Promote the many-to-many relationships between interacting peers to
  "full object status".
  
#### Chain of responsibility (Day 14)

- Avoid coupling the sender of a request to its receiver by giving
  more than one object a chance to handle the request. Chain the
  receiving objects and pass the request along the chain until an
  object handles it.

- Launch-and-leave requests with a single processing pipeline that
  contains many possible handlers.

#### 





# Preparation for the exam

##  Review diagrams/implementations of software design patterns. E.g.,

- sourcemaking (refactoring guru)

https://sourcemaking.com/design_patterns

More info, diagrams and examples of the design patterns you can find 
on the related link:

https://refactoring.guru/design-patterns

- tutorialspoint
https://www.tutorialspoint.com/design_pattern/

- geeksforgeeks (not so organized)
https://www.geeksforgeeks.org/software-design-patterns/

## Consultation hours 
- next week: Monday-Tuesday-Wednesday, 9-16)

## Classroom exercises
- By Sunday night. Please, send comments/corrections.

# Classroom exercise

- "Encrypted" mathematical expressions: A(B(A(4, 5), 5))
- A, B, C, D: chosen from {*, +, -, /}
- The client is interested in:
  - "evaluate" the expressions: i.e., to choose values from {A, B, C, D}
and "evaluate" the resulting expression.
  - "print" the expression: e.g., prefix, infix
  - "search" within the expressions: 
e.g., "the maximum integer", "the number of 'A's", etc.

- You are the class provider. 
- You want to hide from the client:
  - the internal structure chosen to represent mathematical expressions.

- You want to ease for the client the implementation of the programs 
that it is interested in.
  - to "input" an expression, the client simply 
pass a String.



