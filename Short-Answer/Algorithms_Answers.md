#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a)
The runtime complexity of this algorithm is O(N) because the only variable the algorithm depends on is N, and there is only one loop. A is a constant, so despite the amount of arithmetic occurring, since N is the only number that can fundamentally change the scope of the runtime, it is said to be O(N).

b)
The runtime complexity of this algorithm is O(N Log N). I know this because there are two loops, one nested inside of the other, that have dependence on N. However, the inner loop, which depends on approaching N, increases exponentially, so the time to reach N is halved. With this being said, instead of O(N^2), the time complexity is O(N Log N)

c)
The runtime complexity of this algorithm is O(N). This is due to the bunnyEars function having a single recursive callstack, and resolving once bunnies reaches 0. The single dependency and isolated callstack means that this function resolves once one condition is met, making this be the O(N) complexity.

## Exercise II

The strategy that I would take is to minimizes the number of dropped and broken eggs would be as follows

- Since the floors of a building have to be sorted in order, I would implement a binary search algorithm to determine the floor of F at which an egg breaks. - Next, I would slice the number of floors(f) in half, and drop an egg at that middle floor.
- If the egg breaks at this middle floor, we have one broken egg, one dropped egg, and eliminated the floors above that middle floor.
- After this, I would start making my way down on the floors until I reach the point where the eggs no longer break.
- If the egg did not break at the half way point when first tested, reverse the steps and work your way up the floors until the egg breaks.

  -This provides a blanace of eggs dropped and eggs broken. It also brings us a efficient runtime complexity of O(log N), which is faster than O(N)
