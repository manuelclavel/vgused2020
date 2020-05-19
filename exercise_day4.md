# Day 4
## Review
### Creational patterns
-  The basic form of object creation could result in design problems 
or added complexity to the design. 

- Creational design patterns solve this problem by somehow 
**controlling** this object creation.
- Factory Method
  - new is considered harmful
  - basic: hide "constructor" from client.
- Prototype
  - new is considered harmful
  - co-opt one instance of a class for use as a breeder of all future instances.
  - more advance: hide "constructor" from client; creaty by copying/cloning



## Classroom exercise
### Context
- Different types of events/resources(e.g., spaces, machines): 
zumba classes, badminton courts, bykes,...
- Different sports centers (in different cities).
- Different sport centers can apply different "rules"/"values"
for booking the different events/resources. 
  - the holidays/days-off may differ.
  - the operating hours may differ.
  - the events/resources they offer may differ.
  - (*) the price/cost of each event/resource may differ
  - ...
### Problem
- How to implement the creation of bookings, in such a way
that we can more easily "maintain" the application in the
future (e.g, adding more
events/resources, adding more sport centers, etc.) 
  - For the sake of this exercise, assume that each sport center
set a different price for zumba classes, and also for 
badminton courts.






