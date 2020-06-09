## Classroom exercise
 
 [Text borrowed from:  https://www.cs.bu.edu/teaching/c/tree/breadth-first/]

### Helper data structure:

Certain programming problems are easier to solve using multiple data structures.

For example, testing a sequence of characters to determine 
if it is a palindrome 
(i.e., reads the same forward and backward, like "radar") 
can be accomplished easily with one stack and one queue. 
The solution is to enter the sequence of characters into 
both data structures, then remove letters from each data structure 
one at a time and compare them, making sure that the letters match.

In this palindrome example, the user (person writing the main program) 
has access to both data structures to solve the problem. 
Another way that 2 data structures can be used in concert is 
to use one data structure to help implement another.


### Depth-first traversal:

Suppose the following tree:

          tree
          ----
           j    <-- root
         /   \
        f      k
      /   \      \
     a     h      z
      \
       d

A **preorder** traversal would visit the elements in the order: 
j, f, a, d, h, k, z.

This type of traversal is called a **depth-first traversal**. 
Why? Because it tries to go deeper in the tree before 
exploring siblings. 
For example, the traversal visits all the descendants of f 
(i.e., keeps going deeper) before visiting f's sibling k 
(and any of k's descendants).


The 2 other traversal orders we know are **inorder** and **postorder**. 
An inorder traversal would give us: a, d, f, h, j, k, z. 
A postorder traversal would give us: d, a, h, f, z, k, j.

Well, inorder and postorder traversals, like a preorder traversal, 
also try to go deeper first...

For example, the inorder traversal visits a and d before 
it explores a's sibling h. Likewise, it visits all of j's 
left subtree (i.e., "a, d, f, h") 
before exploring j's right subtree (i.e., "k, z"). 
The same is true for the postorder traversal. It visits all 
of j's left subtree (i.e., "d, a, h, f") 
before exploring any part of the right subtree (i.e., "z, k").

### Breadth-first traversal ###

Depth-first is not the only way to go through the elements of a tree. 
Another way is to go through them level-by-level.


Suppose the following tree:

          tree
          ----
           j         <-- level 0
         /   \
        f      k     <-- level 1
      /   \      \
     a     h      z  <-- level 2
      \
       d             <-- level 3

(Computer people like to number things starting with 0.)

So, if we want to visit the elements level-by-level 
(and left-to-right, as usual), we would start at level 0 with j,
then go to level 1 for f and k, then go to level 2 for a, h and z, 
and finally go to level 3 for d.

This level-by-level traversal is called a breadth-first traversal
because we explore the breadth, i.e., full width of the tree at a given 
level, before going deeper.

### Base code

    // Tournament
    public abstract class Tournament {
	
      protected Player winner;
	  protected Player playerA;
	  protected Player playerB;
	  
	  public Player getWinner() {
		return winner;
	}
	}
	
	// SinglesBadminton
	public class SinglesBadminton extends Tournament {

    }
	
	//  SinglesBadmintonTournament
	public class SinglesBadmintonTournament extends Tournament {
 	  private TournamentWithIterator leftBracket;
	  private TournamentWithIterator rightBracket;
	
	  public SinglesBadmintonTournament(Tournament leftBracket, 
	     Tournament rightBracket) {
		this.leftBracket = leftBracket;
		this.rightBracket = rightBracket;
		this.playerA = this.leftBracket.getWinner();
		this.playerB = this.rightBracket.getWinner();
	}
	}
	
	
	
