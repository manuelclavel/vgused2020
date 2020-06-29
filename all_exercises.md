# Factory method (Day 2)
- There are bookings of different types: e.g., badminton, zumba, or
bike-rental.  Each type follows its own "behavior" when the client
creates bookings of this type.
- The clients should not have access to the "new" operator.
- Provide the client with a solution for creating bookings 
of each of the different types.


# Prototype (Day 3)
- There are bookings of different types: e.g., badminton, zumba, or
bike-rental.
- The Consortium requires that bookings include a "code", which is
"expensive" to obtain/generate. This "code" will be the same for all
bookings of the same type and date.
- Provide the client with an effective solution for creating bookings
of each of the different types.

# Abstract Factory (Day 4) 
- There are different types of bookings:
e.g., zumba, badminton, or bike-rental.
- There are different types of sport centers.
- Each sport center may apply different "rules"
for bookings, depending on the type of the booking:
e.g., the price is different
for each type of booking and for each sport center,
and it depends on a value that it can only be
known at the time of the booking.
- These "rules" may change in the future. Also
the sport centers may change in the future, 
as well as the type of bookings available
at each sport center.
- Provide the client with a
solution for creating bookings of each of the
different types,  and for each of the different sport centers.
This solution should be such that it
can be (more) easily maintained in the future. 

# Singleton (Day 5)

- In the solution to the previous exercise, make sure that there is at
most one  "booking factory" for each sport center, and that this "factory" is
available to the customer.

# Adapter (Day 6)
- There are bookings of different types: e.g., zumba, badminton.
- The client should be allowed to "extend a booking" (i.e., 
to extend the duration of the booking).
- Unfortunately the team implementing zumba bookings and
the team implementing badminton bookings have provided 
different interfaces for "extend a booking".
- Provide the client with a solution so that it can (more)
easily "extend a booking" without having to distinguishing 
between zumba and badminton bookings.

# Facade (Day 7)
- There are certain "actions" that require performing
a number of "operations" in the system, in a specific
order. E.g., extending one week a  zumba booking
made with a card does require canceling
first the booking and refunding the amount to the card, before a new booking
is created for the following week. 
- Provide the client with a solution so that it can (more)
easily "extend one week a booking" without having to know
the "operations" involved, or the ordering
of these operations.

# Decorator (Day 8)
- There are bookings of different types: e.g., badminton
and zumba.
- Bookings can also include "optional" features: e.g., cabinet
and shower. "Optional" features may be added to a booking
at any time, in no specific order.
- The type of bookings, and the "optional" features may
be extended in the future.
- Provide the client with a solution so that it can (more)
easily create bookings of each of the 
different types with different "options".

# Composite (Day 9)
- The consortium organized bracket singles-badminton tournaments, 
with different number of participants.
- Provide the client with a solution so that it can
(more) easily "operate" on the tournaments: e.g., 
to book the  tournament games.

# Iterator (Day 10)
- The consortium organized bracket singles-badminton tournaments, 
with different number of participants. Participants in the tournament
must declare their age.
- The client does not know the solution chosen to
"implement" the tournaments.
- Provide the client with a solution so that it can
"traverse" the tournament (the specific 
"traversing" strategy is not relevant): e.g., to list
the participants in the tournament, or to  find
the youngest participant in the tournament.

# Visitor (Day 11)
- The consortium organized bracket  badminton tournaments, 
with different number of participants. There also different 
types of matches in the tournament: e.g., singles and doubles,
for men and for  women. 

- Provide the client with a solution so that it can
(more) easily define "operations" to be performed on
the tournaments: e.g., to get the list of all matches, indicating
for each match the type of the match (singles/doubles, men/women), as well
as the name of the players.

# Observer (Day 12)

- Sport centers organize zumba classes. Players and trainers may
be interested in receiving updates regarding some of these classes.
- Provide the client with a solution so that it can 
(more) easily define the "behavior" of  players and trainers,
when there are changes in the  state of the zumba classes that
they are interested in.

# Mediator (Day 13)
- In a sport center there are players and trainers. A player may 
have several trainers, and a trainer may train several
players. 
- Provide the client with a solution so that it can
(more) easily define the "interaction"
between players and trainers  (e.g., updating each
other about their respective "status"), without providing the trainers
"direct" access to their players, and vice versa.

# Chain of responsibility (Day 14) 
- In a sport center there are different badminton courts that
can "handle" a booking request (e.g., to "accept" the booking
request, if the court is available).
- The client does not know how many badminton courts there 
are in a sport center, and has no "direct" access to any 
of them.
- Provide the client wit a solution so that it can
(more) easily give to more than one badminton court the "chance"
to handle a booking request.
