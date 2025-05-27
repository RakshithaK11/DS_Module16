# Ex18 B-Tree
## DATE:
## AIM:
To write a C function to delete an element in a B Tree.
## Algorithm
1.Search the key k to delete in the B-Tree starting from root.
2.If key k is found in a leaf node, delete it directly.
3.If key k is in an internal node, replace it with predecessor or successor and delete recursively.
4.If the child node has less than minimum keys, borrow from sibling or merge with sibling.
5.Continue fixing the tree during the upward recursion to maintain B-Tree properties.
 

## Program:
~~~

Program to write a C function to delete an element in a B Tree
Developed by: RAKSHITHA K
RegisterNumber: 212223110039

void delete(int item, struct BTreeNode *myNode) {
  int flag;

  if (!myNode) {
    return;
  }

  flag = delValFromNode(item, myNode);

  if (!flag) {
    return;
  }
  if (myNode == root && root->count == 0) {
    root = root->linker[0];
  }


}
~~~

## Output:
![image](https://github.com/user-attachments/assets/ec88a3f5-7382-41be-8f19-ba5597df9a3f)

## Result:
Thus, the C function to delete an element in a B Tree is implemented successfully.
