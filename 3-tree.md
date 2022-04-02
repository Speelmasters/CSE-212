# Tree
A Tree is a non-linear data structure that uses nodes that branch from a root node. The branch nodes are attached based on a condition when the structure is created. In a Bianary Tree, the node is attached based on whether the value is greater or lesser than the current value. An example of a Tree in coding would the the computer file system. 

In this lession, we will be looking at one of the most basic tree structures, the Binary Tree. It is call this because it has at most two child nodes. The nodes consist of the data stored and two pointers. These pointer point to the next node below it, making it look like a tree. In the image below, we can see a parent node(the circle at the top containing 5) and the barnches down to each nod below it. This tree adds the next value based off of the top nodes value. If it is less than the value, it branches to the left, and if it is greater than the value, it branches to the right. This is one of the main benifits of a tree. It has a similar space complexity of a linked list, but has a faster search function as it uses checks to finds values.

![Tree](tree.png)

## Tree Methods

### Insert
The `insert()` method is used to add an item to the tree based on the preset condition. In a Binary tree, it compares the value as the current node, and branches to the right or left untill there is no refernce on the following branch. 

### Contains
The `contains` method is used to check if the specified value is present within the tree. If traverses the tree similar to the insert method, but returns a boolean of true if it finds a node with the designated value.

## Example: Binary Tree
For this example, here is an [example](trees_incomplete.py) of a binary tree that can be built and used in Python. A majority of this class has copyright by BYUI, and as such make no claim to the code. I have included a few changes and implimented some functions. 

## Problem to Solve: Add a remove method
For the problem, you will impliment a remove method. This method will remove the branch that contains the value specified.

Once you have finished your implimentations of the method above, take a look at this possible [solution](trees_solution.py) and compare ways to solve the problems. 
