# DS_Module15

## AIM: 
~~~
To Implement the program for Tree Expression and Traversal using c program.
a) Binary Search Tree
~~~
## PROGRAMS:
### BINARY SEARCH TREE 
```
#include <stdio.h>
#include <stdlib.h>
struct node
{
   int info;
   struct node *left, *right;
};
struct node *createnode(int key)
{
   struct node *newnode = (struct node*)malloc(sizeof(struct node));
   newnode->info = key;
   newnode->left = NULL;
   newnode->right = NULL;
   return(newnode);
}
void inorder(struct node *root)
{
   if(root != NULL)
   {
       inorder(root->left);
       printf(" %d ",root->info);
       inorder(root->right);
   }
}
void largest(struct node *root)
{
   while (root != NULL && root->right != NULL)
   {
       root = root->right;
   }
   printf("\nLargest value is %d", root->info);
}


int main()
{
  /* Creating first Tree. */
   struct node *newnode = createnode(25);
   newnode->left = createnode(17);
   newnode->right = createnode(35);
   newnode->left->left = createnode(13);
   newnode->left->right = createnode(19);
   newnode->right->left = createnode(27);
   newnode->right->right = createnode(55);
   
   printf("Inorder traversal of tree 1 :");
   inorder(newnode);
   largest(newnode);
   
return 0;
}
```

## OUTPUT 
### BINARY SEARCH TREE
![image](https://github.com/user-attachments/assets/b1b0c83f-ee61-4abd-9d54-43b3d949afdc)




