# Read - Trees

Source: [Trees](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

![Binary tree](assets/tree-example.png)

## Terms

* Root - top-most node
* Leaf - a node with no children
* Edge - a connection - the link between parent and child.
* Height - # of edges to bottom-most node
* Depth - # of edges to a node from the top of the tree
* Depth first traversal: prioritizes going through the height of the tree first.
* Breadth first traversal: prioritizes going across the tree level by level

## Traversal

### Depth first

#### Pre-order

root -> left -> right
A, B, D, E, C, F

```javascript
function preOrder(root) {
    console.log(root.value); //or whatever operation you need to perform on each node. 
    if (root.left) preOrder(root.left);
    if (root.right) preOrder(root.right);
}
```

#### In-order

left -> root -> right
D, B, E, A, F, C

```javascript
function inOrder(root) {
    if (root.left) preOrder(root.left);
    console.log(root.value); //or whatever operation you need to perform on each node. 
    if (root.right) preOrder(root.right);
}
```

#### Post-order

left -> right -> root
D, E, B, F, C, A

```javascript
function postOrder(root) {
    if (root.left) preOrder(root.left);
    if (root.right) preOrder(root.right);
    console.log(root.value); //or whatever operation you need to perform on each node. 
}
```

### Breadth first

goes layer by layer using a queue. every time you dequeue a node, you enqueue its children.
A, B, C, D, E, F

```javascript
function breadthFirst(root) {
    const queue = new Queue();
    queue.enqueue(root);
    while (queue.peek) {
        var frontNode = queue.dequeue();
        console.log(frontNode.value); //or whatever operation you need to perform on each node. 
    }
    if (frontNode.left) queue.enqueue(front.left);
    if (frontNode.right) queue.enqueue(front.right);
}
```

## Binary Trees

* If not sorted, then node insert is O(n) and search is O(n) because it's not organized.
* worst case height is n, hence why it's O(n)
* Breadth first insertion is O(w) where w is the largest width of the tree.
* A perfect or balanced binary tree is one where non-leaf nodes all have exactly 2 children. It's max width is 2^(h-1) where h is the height of the tree, aka log(n).

## Binary Search Trees

* Sorted tree where left child is smaller than root, right child is larger than root
* Big O is O(h)
* In a balanced BST, the height of the tree is log(n)
