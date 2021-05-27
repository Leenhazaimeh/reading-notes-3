# Trees

## Common Terminology Used In Tress

- **Node**: A node is the individual item/data that makes up the data structure
- **Root**: The root is the first/top Node in the tree
- **Left Child**: The node that is positioned to the left of a root or node
- **Right Child**: The node that is positioned to the right of a root or node
- **Edge**: The edge in a tree is the link between a parent and child node
- **Leaf**: A leaf is a node that does not contain any children
- **Height**: The height of a tree is determined by the number of edges from the root to the bottommost node

### Traversals

- An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node:

- Depth First
- Breadth First

#### Depth First

- Depth first traversal is where we prioritize going through the depth (height) of the tree first

- some methods for depth first traversal:

1. Pre-order: root >> left >> right
2. In-order: left >> root >> right
3. Post-order: left >> right >> root

Given the sample tree above, our traversals would result in different paths:

1. Pre-order: A, B, D, E, C, F
2. In-order: D, B, E, A, F, C
3. Post-order: D, E, B, F, C, A

- Pre-order means that the root has to be looked at first. In our case, looking at the root just means that we output its value. When we call preOrder for the first time, the root will be added to the call stack:

#### Traversal Pseudocode

Pre-order

        ```
        ALGORITHM preOrder(root)
        // INPUT <-- root node
        // OUTPUT <-- pre-order output of tree node's values

            OUTPUT <-- root.value

            if root.left is not Null
                preOrder(root.left)

            if root.right is not NULL
                preOrder(root.right)
        ```

In-order

        ```
        ALGORITHM inOrder(root)
        // INPUT <-- root node
        // OUTPUT <-- in-order output of tree node's values

            if root.left is not NULL
                inOrder(root.left)

            OUTPUT <-- root.value

            if root.right is not NULL
                inOrder(root.right)
        ```

Post-order

        ```
        ALGORITHM postOrder(root)
        // INPUT <-- root node
        // OUTPUT <-- post-order output of tree node's values

            if root.left is not NULL
                postOrder(root.left)

            if root.right is not NULL
                postOrder(root.right)

            OUTPUT <-- root.value
        ```



### Binary Trees

- In all of our examples, we’ve been using a Binary Tree. Trees can have any number of children per node, but Binary Trees restrict the number of children to two (hence our left and right children).

### Big O

The Big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n). Because of the lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree. If we assume that a tree has n nodes, then in the worst case we will have to look at n items, hence the O(n) complexity.

The Big O space complexity for a node insertion using breadth first insertion will be O(w), where w is the largest width of the tree. For example, in the above tree, w is 4.

>> A “perfect” binary tree is one where every non-leaf node has exactly two children. The maximum width for a perfect binary tree, is 2^(h-1), where h is the height of the tree. Height can be calculated as log n, where n is the number of nodes.
