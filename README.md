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
```java
for(int i=0; i<10; i++) System.out.println(i);
for(int j=10; j>0; j--) System.out.println(j);
```
  *  they are also multiplicative T1*T2=O(f(N)g(N))
```java
for(int i=0; i<10; i++) {
    System.out.println(i);
    for(int j=10; j>0; j--) System.out.println(j);
    }
```
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

*  Big O
  *  T(N) = O(f(N))
  *  if there are positive constants c and n0 such that T(N) ≤ cf(N) when N ≥ n0
*  Big Ω
  *  T(N) = Ω(g(N)) 
  *  if there are positive constants c and n0 such that T(N) ≥ cg(N) when N ≥ n0
*  Big Θ
  *  T(N) = Θ(h(N))
  *  if and only if T(N) = O(h(N)) and T(N) = Ω(h(N)) 
*  Little o
  *  T(N) = o(p(N))
  *  if for all positive constants c there exists an n0 such that T(N) < cp(N) when N > n0. 

## Miscellaneous Topics

#### How does the DNS work

*  Send a request to the browser
  *  Checks if it knows URL before it asks the OS
*  After browser and OS check their cache for the IP of URL
  *  The OS calls the resolver 
*  Resolver checks its cache
*  Resolver server is usually your ISP
  *  All resolvers must know where to locate the root server
*  Root server knows where to locate the .COM TLD (top level domain)
*  The root server can tell you where the .COM TLD server is
*  There are 13 Root servers that sit on top of the DNS hierarchy of TLDs
  *  root-servers.net to m.root-servers.net
*  Internet Corporation for Assigned Names and Numbers coordinates most TLDs
*  When a domain is purchased, the domain registrar reserves the name and tells the TLD the authoritative name server that it’s linked to
*  The Authoritative name server knows the IP address
  *  no cached values
  *  no asking someone else
  *  only the real deal
