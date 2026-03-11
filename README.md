#include<stdio.h>
#include<stdlib.h>
Struct node{
Int key;
Struct node *left,*right;
};
Struct node* newNode(int
key){
Struct node* node=(struct
node*)malloc(sizeof(struct
node));
Node->key=key;
Node->left=node-
>right=NULL;
Return node;
}
Struct node* insert(struct
node* root,int key){
If(root==NULL)
Return newNode(key);
If(key < root->key)
Root->left=insert(root-
>left,key);
Else
Root->right=insert(root-
>right,key);
Return root;
}
Void inorder(struct node*
root){
If(root){
Inorder(root->left);
Printf(“%d “,root->key);
Inorder(root->right);
}
}
Int main(){
Struct node* root=NULL;
Root=insert(root,70);
Root=insert(root,85);
Root=insert(root,60);
Printf(“Student Marks (AVL
Tree): “);
Inorder(root);
Return 0;
}
OUTPUT
Student Marks (AVL Tree): 60
70 85
