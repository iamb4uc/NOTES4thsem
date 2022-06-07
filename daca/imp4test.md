### What is an Algorithm?

An algorithm is a finite set of instructions that if followed, accomplishes a particular task. All algorithm must satisfy the following criteria:

-   Input
-   Output
-   Definiteness
-   Definiteness
-   Effectiveness  

### Algorithm to find and return the maximum of n given numbers.

    MAXIMUM

    Step1: Set Max = 0

    Step2: while (i != n)
             if(i > MAX)
               Set Max = A[i];
             else
               return;

    Step3: Print(Max)

    Step4: Exit

### Analysis of Algorithm

A complete analysis of an algorithm involves the following steps:  

1.  Implement the algorithm correctly.
2.  Determine the time required for each basic operations.
3.  Identify unknown quantities that can be used to describe the frequency of execution of basic operation.
4.  Develop a realistic model for the input to the program.
5.  Analyze the unknown quantities assuming the model input.
6.  Calculate the total running time by multiplying the time by the frequency for each operation and then adding all the products.

### Why analysis of algorithm is important.

1.  To predict the behavior of algorithm without implementing it on a specific machine.
2.  It is impossible to predict the exact behavior of an algorithm as their are too many influencing factors. The analysis is thus only an approximation, not perfect.
3.  By analyzing different algorithm, we can compare them to determine the best one for our purpose.

### Asymptotic Analysis

It is a technique of representing limited behavior. It can be used to analyze the performance of an algorithm for some large dataset.  
![eg](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%20f%28n%29%3Dn%5E2+3n)  
In the above function, the term ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%203n) becomes insignificant compared to ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%20n%5E2) when ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%20n) is very large.  

### Why is Asymptotic Notation important?

1.  They give simple characteristics of an algorithm's efficiency.  
2.  It allows the comparison of the performance of various algorithm.

### Asymptotic Notation
Asymptotic notation are used to describe the running time of an algorithm.  
There are 3 notations used for describing the running time of the algorithm.
1. Big-oh Notation(O-notation): When we have an asymptotic upper-bound, we use O-notation. The O-notation is used when the function f(n) is defined as:  
![equation](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%20f%28n%29%3DO%28g%28n%29%29%5C%3A%20%5Cexists%5C%3A%20positive%5C%3A%20constant%5C%3A%20C%5C%3A%20and%5C%3A%20n_0)  
Such that  
![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%20f%28n%29%5Cleqslant%20cg%28n%29%5C%3B%20%5Cforall%5C%3B%20n%20%5Cgeqslant%20n_0)

Graphically, we represent O notation as follows:  
![diagram](img/big-oh-graph.png)  

2. Omega Notation (Ω-notation): The Ω notation is used when the function g(n) defines a lower-bound for the function f(n) which is defined as  
![f(n)=\Omega (g(n)), \exists\; two \; positive \; constants\; C\; and \; n_0](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%20f%28n%29%3D%5COmega%20%28g%28n%29%29%2C%20%5Cexists%5C%3B%20two%20%5C%3B%20positive%20%5C%3B%20constants%5C%3B%20C%5C%3B%20and%20%5C%3B%20n_0)  
Such that  
![cg(n)\leqslant f(n)\; \forall\; n\geqslant n_0](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%20cg%28n%29%5Cleqslant%20f%28n%29%5C%3B%20%5Cforall%5C%3B%20n%5Cgeqslant%20n_0)
Graphically we can represent  Ω-notation as  
![](img/omega-graph.png)  

3. Theta Notation (Θ-notation): The Θ-notation is used when the function f(n) is bounded both above and below by the function g(n), which is defined as  
![f(n)=\Theta (g(n)), \exists\; three \; positive \; constants\; c_1,c_2\; and \; n_0](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%20f%28n%29%3D%5CTheta%20%28g%28n%29%29%2C%20%5Cexists%5C%3B%20three%20%5C%3B%20positive%20%5C%3B%20constants%5C%3B%20c_1%2Cc_2%5C%3B%20and%20%5C%3B%20n_0)  
Such that  
![c_1g(n)\leqslant f(n)\leqslant c_2g(n)\; \forall\; n\geqslant n_0](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Cdpi%7B120%7D%20%5Clarge%20c_1g%28n%29%5Cleqslant%20f%28n%29%5Cleqslant%20c_2g%28n%29%5C%3B%20%5Cforall%5C%3B%20n%5Cgeqslant%20n_0)
Graphically we can represent  Θ-notation as  
![](img/theta-graph.png)  

### Stack Algorithm
#### Using Linear Array
##### PUSH
PUSH(STACK, TOP, MAXSTK, ITEM)
This procedure pushes an ITEM onto the STACK
1. [Stack already filled?]  
If TOP = MAXSTK,  
then  
Print "OVERFLOW"  
and Exit.  
2. Set TOP = TOP+1  [Increases TOP by 1]
3. Set STACK[TOP] = ITEM. [Inserts ITEM in new TOP position.]
4. Exit.

##### POP
POP(STACK, TOP, ITEM)  
This procedure deletes the top element of STACK and assigns it to the variable ITEM.  
1. [STACK has an item to be removed?]  
If TOP = 0,  
then  
Print "UNDERFLOW"  
and Exit.
2. Set ITEM = STACK[TOP]. [Assigns TOP element to ITEM.]
3. Set TOP = TOP - 1. [Decrease TOP by 1.]
4. Exit

### Queue Algorithm
##### INSERT
QINSERT(QUEUE, N, FRONT, REAR, ITEM)
This procedure inserts an element ITEM into a queue.

1. [Queue already filled?]
If FRONT = 1 and REAR = N, or if FRONT = REAR + 1,
then
Print "OVERFLOW"
and Exit
2. [Find new value of REAR.]
If FRONT = NULL, then [Queue initially empty.]
Set FRONT = 1 and REAR = 1
Else if REAR = N,
Set REAR = 1
Else
Set REAR = REAR + 1
3. Set QUEUE[REAR] = ITEM. [This inserts new element.]
4. Exit

##### DELETE
QDELETE

### Tree
A tree is a finite set of 1 or more node such that specially designated node for the root and the remaining nodes are partitioned into ![](https://latex.codecogs.com/gif.latex?n%5Cgeqslant%200) disjoint sets T1, ....., Tn are called the subtree of the root.


#### Terminalogy:
![](img/tree.png)
1. Root: The root node is the topmost node in the tree hierarchy. In the above structure node 1 is the root node of the tree and would be called a parent-child relationship.  

2. Child node: If the node is the descendant of any node then the node is known as a child node.  

3. Parent node: If a node contains any sub-node then the node is called a parent node.

4. Sibling node: The node that have a same parent are known as sibling node.

5. Ancestor node: An ancestor of a node is an predecessor node on any path from root of that node. 1, 2, and 5 are the ancestors of 10.

6. Descendant: The immediate successor of the given node is known as descendant of a node. 10 is the descendant of node 5.

7. Leaf: In a tree data structure, the node which does not have a child is called as LEAF Node. In simple words, a leaf is a node with no child.


### Binary tree
A binary tree is a finite set of node i.e. either empty or consists of a root and two disjoint binary trees called the left and right subtree.

***Note:  
The maximum number of nodes on level "i" of a binary tree is 2^(i-1) also the maximum number of nodes in a binary tree of depth k is 2^k - 1, K > 0.***


### Binary Search Tree (BST)
A BST is a binary tree which may be empty. If it is not empty, then, it satisfy the following properties:  
1. Every element has a key and no two elements have the same key.  
2. The keys in the left subtrees are smaller than the key in the root.  
3. The keys in the right subtrees are larger then the key in the root.
4. The left and right subtrees are also BST.  

*Example: Create a BST from the following data element.*
```45,15,79,90,10,55,12,20,50```  
**Solution** ![](img/bstex.png)  

### Write an algorithm to delete an element x from a binary search tree t.
#### Algorithm for deleting a node from a binary search tree
Suppose R is a binary search tree and suppose an ITEM of information is given. The deletion algorithm first find the location of the node N which contains ITEM and also the location of the parent node P(N).  
The way N is a deleted from the true depend primarily on the number of children of node N.  
There are 3 cases:  

**Case I**: N has no children  
Then N is deleted from R by simply replacing the location of N in the parent node P(N) by the NULL pointer.  

**Case II**: N has exactly one child. Then N is deleted from T by simply replacing the location of N in P(N) by location of the only child of N.  

**Case III**: N has two children. Let S(N) denote the node succession of N. Then N is deleted from T by first deletion S(N) from T and then replacing number N in T by the node S(N).


Let us take an example - In the following fig, the node 50 is to be deleted which is the root node of the tree. The in-order traversal of the tree given below:  
```6, 25, 30, 50, 52, 60, 70, 75.```  
Replace 50 with its in-order successor 52. Now, 50 will be moved to the leaf of the tree, which will simply be deleted.
![](img/deletenode.png)  
The Algorithm is as follows  

```
Delete (TREE, ITEM)
IF TREE = NULL
  Write "item not found in the tree"
ELSE IF ITEM < TREE -> DATA
  Delete(TREE->LEFT, ITEM)
ELSE IF ITEM > TREE -> DATA
  Delete(TREE -> RIGHT, ITEM)
ELSE IF TREE -> LEFT AND TREE -> RIGHT
  SET TEMP = findLargestNode(TREE -> LEFT)
  SET TREE -> DATA = TEMP -> DATA
  Delete(TREE -> LEFT, TEMP -> DATA)
ELSE
  SET TEMP = TREE
IF TREE -> LEFT = NULL AND TREE -> RIGHT = NULL
  SET TREE = NULL
ELSE IF TREE -> LEFT != NULL
  SET TREE = TREE -> LEFT
ELSE
  SET TREE = TREE -> RIGHT
[END OF IF]

FREE TEMP
[END OF IF]

Exit
```
### Time Complexity:  
The worst case time complexity of delete operation is O(h) where h is the height of the Binary Search Tree. In worst case, we may have to travel from the root to the deepest leaf node. The height of a skewed tree may become n and the time complexity of delete operation may become O(n).  

### Show that the height of a binary tree that has n, n > 0, nodes is at most n and at least ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5B%5Clog_2%28n&plus;1%29%5D).  
The minimum number of nodes in a binary tree t whose height is h, all possible roots at first h levels are ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%202%5Eh%20-%201)  
Let n be the number of nodes in a binary tree where height is denoted by h, then  
![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20h%5Cleqslant%20n%5Cleqslant%202%5En-1%5C%5C%20or%5C%3B%20%5Clog_2%20%28n&plus;1%29%5Cleqslant%20h%5Cleqslant%20n)  

### What is the maximum number of nodes in a binary tree that has m leaves.  
A complete binary tree always has ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%202%5Em) leaves for some value of m.  

Starting from the root, it has 2 children, and 4 total children of those children, and so on, up to and including the ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%202%5Em) leaves. So summing up total number of nodes will be,  
![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%201&plus;2&plus;4&plus;8&plus;...&plus;2%5Em%3D%5Csum_%7Bi%3D0%7D%5E%7Bm%7D2%5Ei)  

![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%5Csum_%7Bi%3D0%7D%5E%7Bm%7D2%5Ei%3D2%5E%7Bm&plus;1%7D-1)  

Let ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20n%3D2%5Em), the number of leaves.  
Then ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%202%5E%7Bm&plus;1%7D-1%3D2*2%5Em-1%3D2n-1) which is the total number of nodes.  
(The number of leaf nodes in a full binary tree with n nodes equal to ![](https://latex.codecogs.com/svg.latex?%5Cinline%20%5Clarge%20%28n&plus;1%29/2))
