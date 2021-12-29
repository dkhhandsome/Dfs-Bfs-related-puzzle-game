# Dfs-Bfs-related-puzzle-game


## Sudoku

This puzzle commonly appears in print media and online. You are presented with an n × n grid with some symbols, for example digits or letters, filled in. The symbols must be from a set of n symbols. The goal is to fill in the remaining symbols in such a way that each row, column, and subsquare, contains each symbol exactly once. In order for all of that to make sense, n must be a square integer such as 4, 9, 16, or 25.

## Word Ladder

This puzzle involves transforming one word into a target word by changing one letter at a time. Each word must belong to a specified set of valid words. Here’s an example where we assume that the set of valid words is a rather large set of common English words, and the goal is to get from the word ‘cost’ to the word ‘save’:

cost → cast → case → cave → save

## Expression Tree Puzzle

This puzzle consists of an algebraic equation containing one or more variables, and a target value. The puzzle is solved when the variables are assigned values such that the expression evaluates to the target value.


## The search algorithms

Depth-first search and breadth-first search are two approaches to searching through the space of possibilities for a solution.


**dfs

With depth-first search, we search deeply before we search broadly.  We exhaustively search the first subtree before considering any other subtree.  And we use the same strategy when we search that subtree: exhaustively searching its first subtree before considering any other subtree.  And so on - think recursively!

**bfs

With breadth-first search, we search broadly before we search deeply. We consider all puzzle states at depth 1, then all puzzle states at depth 2, and so on until we have searched all puzzle states in our tree.  (You will find a queue is helpful for keeping track of puzzles states to be checked when their turn comes.) Because we consider states that are “closer” to the starting state before those that are “farther”, we are guaranteed to find the shortest path to a puzzle’s solution.

For both solvers, we run the risk of encountering a puzzle state that we've already seen, and which already failed to produce a solution. To avoid exploring that state all over again, we will keep track of states we've seen before and just ignore them if we encounter them again.

For certain puzzle types, we might also be able to check whether we can quickly tell if a puzzle state is unsolvable. Such a check can be incorporated into our search algorithms and you will do so in your implementation.

Rather than spell out the algorithms in full detail and simply have you translate them into code, we have put together some worked examples - one of your tasks in this assignment will be to turn the above high level descriptions and the concrete examples into 2 algorithms you can implement in Python!
