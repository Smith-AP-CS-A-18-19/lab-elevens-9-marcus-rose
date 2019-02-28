# Elevens 9

Follow the instructions provided for Activity 9 in the student lab guide. Complete the necessary methods and ensure that your game is running properly. You may need to run it from the command line to have it recognize the card graphics. Answer the questions below before you push the finalized repo.

## Questions
1. The size of the board is one of the differences between *Elevens* and *Thirteens*. Why is size not an abstract method?

    The size of the board is not constant and changes depending on the two games; it is an abstract method because it is a relative aspect of the board depending on the game.

2. Why are there no abstract methods dealing with the selection of the cards to be removed or replaced in the array `cards`?

  Selection/removal methods do not need to be abstract because the removal/replacing of each card is consistent throughout any board.

3. Another way to create “IS-A” relationships is by implementing interfaces. Suppose that instead of creating an `abstract Board` class, we created the following `Board` interface, and had `ElevensBoard` implement it. Would this new scheme allow the Elevens GUI to call `isLegal` and `anotherPlayIsPossible` polymorphically? Would this alternate design work as well as the `abstract Board` class design? Why or why not?
	```java
	public interface Board {
	    boolean isLegal(List<Integer> selectedCards);
	    boolean anotherPlayIsPossible();
	}
	```

    The new scheme would allow for the calls described above because the ElevensBoard class implements this new interface, and the two methods are in the interface. The alternate design works too because an abstract method is without implementation: it has access to these methods, but they are simply empty. So, ElevensBoard will have access to the methods in this interface because ElevensBoard implements Board.
