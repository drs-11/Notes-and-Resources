# Algorithms

---

### Backtracking

In order to apply backtracking to a specific class of problems, one must provide the data *P* for the particular instance of the problem that is to be solved, and six procedural parameters, *root*, *reject*, *accept*, *first*, *next*, and *output*. These procedures should take the instance data *P* as a parameter and should do the following:

1. *root*(*P*): return the partial candidate at the root of the search tree.
2. *reject*(*P*,*c*): return *true* only if the partial candidate *c* is not worth completing.
3. *accept*(*P*,*c*): return *true* if *c* is a solution of *P*, and *false* otherwise.
4. *first*(*P*,*c*): generate the first extension of candidate *c*.
5. *next*(*P*,*s*): generate the next alternative extension of a candidate, after the extension *s*.
6. *output*(*P*,*c*): use the solution *c* of *P*, as appropriate to the application.

```
procedure backtrack(c) is
    if reject(P, c) then return
    if accept(P, c) then output(P, c)
    s ← first(P, c)
    while s ≠ NULL do
        backtrack(s)
        s ← next(P, s)
```

Optimizations:

- Pruning the search: We can often optimize backtracking by pruning the search tree. The idea is to add ”intelligence” to the algorithm so that it will notice as soon as possible if apartial solution cannot be extended to a complete solution.

- Meet in the middle: Meet in the middleis a technique where the search space is divided into twoparts of about equal size. A separate search is performed for both of the parts,and finally the results of the searches are combined. Typically, we can turn a factor of 2^n into a factor of 2^(n/2) using the meet in the middle technique.

ref: [[1]](https://en.wikipedia.org/wiki/Backtracking), [[2]](https://cses.fi/book/book.pdf)

### Greedy

A greedy algorithm constructs a solution to the problem by always making a
choice that looks the best at the moment. A greedy algorithm never takes back
its choices, but directly constructs the final solution.

In general, greedy algorithms have five components:

1. A candidate set, from which a solution is created
2. A selection function, which chooses the best candidate to be added to the solution
3. A feasibility function, that is used to determine if a candidate can be used to contribute to a solution
4. An objective function, which assigns a value to a solution, or a partial solution, and
5. A solution function, which will indicate when we have discovered a complete solution

ref: [[1]](https://en.wikipedia.org/wiki/Greedy_algorithm)

### Morris Traversal (Tree)

ref: [[1]](https://en.wikipedia.org/wiki/Threaded_binary_tree), [[2]](https://www.geeksforgeeks.org/inorder-tree-traversal-without-recursion-and-without-stack/), [[3]](https://liacs.leidenuniv.nl/~deutzah/DS/september28.pdf)

### Hibbard Node Deletion (Binary Search Tree)

```
    if ( k not in BST )
    {
       return;         // Nothing to delete
    }

    /****** The "Hibbard deletion algorithm" ******/

    if ( k has no subtrees )           //     x            x
    {                                  //    / \    ==>   /
       unlink k from k's parent;       //   y   k        y
       return;                         //
    }

    if ( k has 1 tree )                       //     x            x
    {                                         //    / \    ==>   / \
       make k's parent point to k's subtree;  //   y   k        y   z
       return;                                //        \
    }                                                    z

    /* k has 2 subtrees - TOUGH */

   (1)  find the successor of k:
            go right once
        go left all the way down

   (2) Replace k with k's successor;

   (3) Make the successor's parent point to the successor's right subtree; 
```

ref: [[1]](http://www.mathcs.emory.edu/~cheung/Courses/171/Syllabus/9-BinTree/BST-delete2.html)
