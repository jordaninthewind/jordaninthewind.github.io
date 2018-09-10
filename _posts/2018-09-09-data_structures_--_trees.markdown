---
layout: post
title:      "Data Structures -- Trees"
date:       2018-09-10 01:52:46 +0000
permalink:  data_structures_--_trees
---

### Continuing into data structures...

Trees are another data structure that is frequently encountered when considering possibly more efficient routes in designing algorithms and working with dynamic data sets.

Trees are more like a root system, in common depiction, than trees, but start with a number of consistent (and similarly arboreal) qualities.

A tree is made of nodes that correspond to each other with references and a few rules that work to create a predictable a workable strucutre. Trees are organized with a start node -- trees start with a root. The root is a node that becomes the relative entry/access point to the data structure. A node could be the middle index of a sorted array of numbers and from there the tree could descend in an organized manner as more node values are added.

Nodes will usually have two pointers, a left and a right, each of which should point to a number in reference that is smaller, on the left, and larger, on the right. If a tree starts at a middle index of a sorted array, any numbers that come afterward will be larger and any that come before will be sorted. So, if we would like to flatten the array as much as possible and distribute the array across a tree, we can start in the middle, take the middle of the larger array and begin to for related trees from the tree as it starts.

Trees will always have a left and a right value, if the value is not a number, it will be null.

All numbers lower than the current node will always be added as subtrees to the left while all numbers equal to or greater are always added to the right. This can create balanced trees that will be read by traversal of each node to increase efficiency with predictable rules and form.

The last nodes are called leaves and they will result in an end value of null and the memory stack calling subsequent processes to continue traversal.
