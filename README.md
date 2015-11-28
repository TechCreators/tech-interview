# Coding Interview Tips and Tools
Technical interviews can be **difficult**, but it doesn't have to be. Everyone has their own approach to acing them. Here's my take...

### Table of Contents
*  [Basics](#basics)
  *  Proofs
  *  Runtime Estimation
  *  Recursion
*  [Data Structures](#data-structures)
  *  Arrays
  *  Singly Linked List
  *  Doubly Linked List
  *  Stacks
  *  Queues
  *  AVL Tree
  *  Binary Tree
  *  Min Heap / Max Heap (talk about how we can find the median value using both)
*  [Sorting](#sorting)
  *  Bubble Sort O(N<sup>2</sup>
  *  Selection Sort O(N<sup>2</sup>
  *  Insertion Sort O(N<sup>2</sup>
  *  Merge Sort O(NlogN)
  *  Quick Sort O(NlogN)
*  [Java](#java)
  *  Primitive Types
  *  String
  *  Array / ArrayList
  *  ArrayDeque (stack and queue)
*  [Python](#python)
*  [Miscellaneous Topics](#miscellaneous-topics)
  *  How does the DNS work
  *  Functional Programming
*  [Pass the Phone Screen](#pass-the-phone-screen)
*  [Helpful Resources](#helpful-resources)


## Basics

#### Proofs
Proof by Induction</br>
*  Assert the Base Case
  *  Establish a theorem that is true for some small trivial value
*  Inductive Hypothesis 
  *  The theorem is assumed to be true for all cases up to some limit k
*  Prove True for k+1th case

Proof by Counterexample</br>
* Present a case where the statement is false

Proof by Contradiction</br>
*  Assume the theorem is false
*  Show that the assumption implies that some known property is false, hence the original assumption was erroneous

#### Runtime Estimation

Rules
*  T1(N) = O(f(N)) and T2(N) = O(g(N))
  *  then the sum of T1 and T2  = O(f(N)+g(N))
    *  loops right after one another
  *  they are also multiplicative T1*T2=O(f(N)g(N))
    *  nested loops
*  T(N) is a polynomial degree k then T(N) = Theta(Nk)
*  logk(N) =O(N) for any constant k.
  *  tells us that logarithms grow very slowly


| Big-O  | time complexity |
| ------------- | ------------- |
| O(1)  | constant  |
| O(logN)  | logarithmic  |
|O(N)            | linear      |
|O(NlogN)        |             |
|O(N<sup>2</sup>)| quadratic   |
|O(2<sup>N</sup>)| exponential |
|O(N<sup>N</sup>)|             |


