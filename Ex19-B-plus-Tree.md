# Ex19 B+ Tree
## DATE:
## AIM:
To write a C function to traverse the elements in a B+ Tree.

## Algorithm
1.Start at the current node p.
2.For each key from 0 to p->n-1:
3.If p is not a leaf, recursively traverse p->child_ptr[i].
4.Print the key p->data[i].
5.If p is not a leaf, recursively traverse the last child p->child_ptr[p->n].  

## Program:
~~~
/*
Program to traverse the elements in a B+ Tree.
Developed by: RAKSHITHA K
RegisterNumber: 212223110039

void traverse(struct B_TreeNode *p)
{
    int i;
    for(i=0;i<p->n;i++){
        if(p->leaf==0){
            traverse(p->child_ptr[i]);
        }
        printf("%d ",p->data[i]);
    }
    if(p->leaf==0){
        traverse(p->child_ptr[i]);
    }
} 
*/
~~~

## Output:
![image](https://github.com/user-attachments/assets/f1dea6a6-f62f-40e0-98a7-5cf0bd2e5f10)

## Result:
Thus, the function to traverse the elements in a B+ Tree is implemented successfully.
