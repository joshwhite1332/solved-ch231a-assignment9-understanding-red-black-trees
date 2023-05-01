Download Link: https://assignmentchef.com/product/solved-ch231a-assignment9-understanding-red-black-trees
<br>
<h1></h1>

<ul>

 <li> Draw (or describe by using preorder traversal) the red-black trees that result after successively inserting the values step by step in the following order [13<em>,</em>44<em>,</em>37<em>,</em>7<em>,</em>22<em>,</em>16] into an empty red-black tree. You are required to draw (or describe by using preorder traversal) the tree after each insertion, as well as any additional recoloring and balancing.</li>

 <li>Draw (or describe by using preorder traversal) all valid red-black trees that store the values {1<em>,</em>2<em>,</em>3<em>,</em>4}.</li>

 <li><strong>Bonus </strong> Consider a red-black tree formed by inserting <em>n </em>nodes with the algorithm described in the lecture slides. Prove that if <em>n &gt; </em>1, the tree contains at least one red node.</li>

</ul>

<h1><strong>Problem 9.2 </strong>Implementing Red Black Trees</h1>

Implement a red black tree (with integer nodes), closely following the specifications and algorithms from the lecture. Make sure you handle errors appropriately by printing messages or throwing exceptions. Your implementation has to be along the interface below with the following or equivalent components:

enum Color {RED, BLACK}; struct Node

{ int data; Color color;

Node <sup>∗</sup>left, <sup>∗</sup>right, <sup>∗</sup>parent;

};

class RedBlackTree

{ private:

Node <sup>∗</sup>root; protected:

void rotateLeft(Node <sup>∗</sup>&amp;); void rotateRight(Node <sup>∗</sup>&amp;); public:

RedBlackTree(); void insert(int); void delete(Node <sup>∗</sup>&amp;);

Node <sup>∗ </sup>predecessor(const Node <sup>∗</sup>&amp;);

Node <sup>∗ </sup>successor(const Node <sup>∗</sup>&amp;);

Node <sup>∗ </sup>getMinimum();

Node <sup>∗ </sup>getMaximum();

Node <sup>∗ </sup>search(int); };