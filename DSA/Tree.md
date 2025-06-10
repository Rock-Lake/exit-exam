Trees, similar to [[Linked List|linked lists]] consists of a data node and a pointer. However, its differences are as follows:
```C++
struct Node{
int Num; // Node value/Number
Node * Left, *Right; // Pointer to Left and right Children
};
Node *RootNodePtr=NULL; // pointer to root Node
```
- There is a **root node** that all other nodes will be connected to
- there is is a number of other pointers that point to **subtree** nodes

The most used type of tree structure in algorithms is the **Binary Search Tree**(BST) where each sub tree only have 2 nodes; left and right nodes.

Binary search trees can be traversed in 3 ways:
- **Pre-order traversal** - goes in the order parent, left, right
- **Inorder traversal** - goes in the order left, parent, right
- **Post-order traversal** - goes in the order left, right, parent