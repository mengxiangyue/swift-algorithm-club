![Swift Algorithm Club](/Images/SwiftAlgorithm-410-transp.png)

# 欢迎来到 Swift 算法俱乐部！

在这里你能发现流行的算法和数据结构，并且是使用每个人都喜欢的新语言 Swift 实现的，并且有它们如何工作的详细说明。

如果你是一个需要学习这些东西通过考试的计算机科学专业的学生 -- 或者如果你是一个自学成才的程序员，想要刷新你的技术背后的理论 -- 你来对了地方。

这个项目的目的是**说明算法如何工作**。其关注点是代码逻辑清晰、易读，而不是去制作一个你加入你的项目就能重复使用的库。换句话说，大多数代码都应该可以用于生产，但是您可能需要调整它以适应您自己的代码库。

代码基于 **Xcode 9** 和 **Swift 4**。我们将会保持更新至最新版本的Swift。

:heart_eyes: **欢迎提建议和贡献自己的力量** :heart_eyes:

## 重要链接

[算法和数据结构是什么？](What%20are%20Algorithms.markdown) 煎饼!

[为什么要学习算法和数据结构？](Why%20Algorithms.markdown) 担心这不是你的菜？那就读这篇文章。

[大O表示法笔记](Big-O%20Notation.markdown)。我们经常像这样说：“这个算法复杂度是 **O(n)** ”。如果你不知道这是什么意思，那就读这篇文章。

[算法设计技术](Algorithm%20Design.markdown). 你怎样创建你自己的算法？

[How to contribute](https://github.com/raywenderlich/swift-algorithm-club/blob/master/.github/CONTRIBUTING.md). Report an issue to leave feedback, or submit a pull request.

## 从何开始?

如果你是刚接触算法和数据结构，下面这些是一个比较好的开始：

- [栈 Stack](Stack/)
- [队列 Queue](Queue/)
- [插入排序 Insertion Sort](Insertion%20Sort/)
- [二分查找 Binary Search](Binary%20Search/) and [二分搜索树 Binary Search Tree](Binary%20Search%20Tree/)
- [归并排序 Merge Sort](Merge%20Sort/)
- [Boyer-Moore字符串搜索 Boyer-Moore string search](Boyer-Moore/)

## 算法

### 搜索

- [线性查找 Linear Search](Linear%20Search/). 在数组中查找一个元素。
- [二分查找 Binary Search](Binary%20Search/). 在已经排好序的数组中快速找到一个元素。
- [统计出现次数 Count Occurrences](Count%20Occurrences/).  统计某个值在数组中出现的次数。
- [选择最大/最小值 Select Minimum / Maximum](Select%20Minimum%20Maximum). 在数组中找到最大/最小值。
- [第k大元素 k-th Largest Element](Kth%20Largest%20Element/). Find the *k*-th largest element in an array, such as the median.
- [选择抽样 Selection Sampling](Selection%20Sampling/).  在集合中随机选择一堆元素。
- [联合查找 Union-Find](Union-Find/). 跟踪不相交的集合，并让您快速合并。


### 字符串查找 String Search 

- [Brute-Force String Search](Brute-Force%20String%20Search/). A naive method.
- [Boyer-Moore](Boyer-Moore/). A fast method to search for substrings. It skips ahead based on a look-up table, to avoid looking at every character in the text.
- [Knuth-Morris-Pratt](Knuth-Morris-Pratt/). A linear-time string algorithm that returns indexes of all occurrencies of a given pattern.
- [Rabin-Karp](Rabin-Karp/)  Faster search by using hashing.
- [Longest Common Subsequence](Longest%20Common%20Subsequence/). Find the longest sequence of characters that appear in the same order in both strings.
- [Z-Algorithm](Z-Algorithm/). Finds all instances of a pattern in a String, and returns the indexes of where the pattern starts within the String.

### 排序 Sorting

It's fun to see how sorting algorithms work, but in practice you'll almost never have to provide your own sorting routines. Swift's own `sort()` is more than up to the job. But if you're curious, read on...

基本排序：

- [Insertion Sort](Insertion%20Sort/)
- [Selection Sort](Selection%20Sort/)
- [Shell Sort](Shell%20Sort/)

Fast sorts:

- [Quicksort](Quicksort/)
- [Merge Sort](Merge%20Sort/)
- [Heap Sort](Heap%20Sort/)

Special-purpose sorts:

- [Counting Sort](Counting%20Sort/)
- [Radix Sort](Radix%20Sort/)
- [Topological Sort](Topological%20Sort/)

Bad sorting algorithms (don't use these!):

- [Bubble Sort](Bubble%20Sort/)
- [Slow Sort](Slow%20Sort/)

### Compression

- [Run-Length Encoding (RLE)](Run-Length%20Encoding/). Store repeated values as a single byte and a count.
- [Huffman Coding](Huffman%20Coding/). Store more common elements using a smaller number of bits.

### Miscellaneous

- [Shuffle](Shuffle/). Randomly rearranges the contents of an array.
- [Comb Sort](Comb%20Sort/). An improve upon the Bubble Sort algorithm.
- [Convex Hull](Convex%20Hull/).
- [Miller-Rabin Primality Test](Miller-Rabin%20Primality%20Test/). Is the number a prime number?
- [MinimumCoinChange](MinimumCoinChange/). A showcase for dynamic programming.

### Mathematics

- [Greatest Common Divisor (GCD)](GCD/). Special bonus: the least common multiple.
- [Permutations and Combinations](Combinatorics/). Get your combinatorics on!
- [Shunting Yard Algorithm](Shunting%20Yard/). Convert infix expressions to postfix.
- [Karatsuba Multiplication](Karatsuba%20Multiplication/). Another take on elementary multiplication.
- [Haversine Distance](HaversineDistance/). Calculating the distance between 2 points from a sphere.
- [Strassen's Multiplication Matrix](Strassen%20Matrix%20Multiplication/). Efficient way to handle matrix multiplication.

### Machine learning

- [k-Means Clustering](K-Means/). Unsupervised classifier that partitions data into *k* clusters.
- k-Nearest Neighbors
- [Linear Regression](Linear%20Regression/). A technique for creating a model of the relationship between two (or more) variable quantities.
- Logistic Regression
- Neural Networks
- PageRank
- [Naive Bayes Classifier](Naive%20Bayes%20Classifier/)

## 数据结构

The choice of data structure for a particular task depends on a few things.

First, there is the shape of your data and the kinds of operations that you'll need to perform on it. If you want to look up objects by a key you need some kind of dictionary; if your data is hierarchical in nature you want a tree structure of some sort; if your data is sequential you want a stack or queue.

Second, it matters what particular operations you'll be performing most, as certain data structures are optimized for certain actions. For example, if you often need to find the most important object in a collection, then a heap or priority queue is more optimal than a plain array.

Most of the time using just the built-in `Array`, `Dictionary`, and `Set` types is sufficient, but sometimes you may want something more fancy...

### Variations on arrays

- [Array2D](Array2D/). A two-dimensional array with fixed dimensions. Useful for board games.
- [Bit Set](Bit%20Set/). A fixed-size sequence of *n* bits.
- [Fixed Size Array](Fixed%20Size%20Array/). When you know beforehand how large your data will be, it might be more efficient to use an old-fashioned array with a fixed size.
- [Ordered Array](Ordered%20Array/). An array that is always sorted.
- [Rootish Array Stack](Rootish%20Array%20Stack/). A space and time efficient variation on Swift arrays.

### Queues

- [Stack](Stack/). Last-in, first-out!
- [Queue](Queue/). First-in, first-out!
- [Deque](Deque/). A double-ended queue.
- [Priority Queue](Priority%20Queue). A queue where the most important element is always at the front.
- [Ring Buffer](Ring%20Buffer/). Also known as a circular buffer. An array of a certain size that conceptually wraps around back to the beginning.

### Lists

- [Linked List](Linked%20List/). A sequence of data items connected through links. Covers both singly and doubly linked lists.
- [Skip-List](Skip-List/). Skip List is a probablistic data-structure with same logarithmic time bound and efficiency as AVL/ or Red-Black tree and provides a clever compromise to efficiently support search and update operations.

### Trees

- [Tree](Tree/). A general-purpose tree structure.
- [Binary Tree](Binary%20Tree/). A tree where each node has at most two children.
- [Binary Search Tree (BST)](Binary%20Search%20Tree/). A binary tree that orders its nodes in a way that allows for fast queries.
- [Red-Black Tree](Red-Black%20Tree/). A self balancing binary search tree.
- [Splay Tree](Splay%20Tree/). A self balancing binary search tree that enables fast retrieval of recently updated elements.
- [Threaded Binary Tree](Threaded%20Binary%20Tree/). A binary tree that maintains a few extra variables for cheap and fast in-order traversals.
- [Segment Tree](Segment%20Tree/). Can quickly compute a function over a portion of an array.
- [Lazy Propagation](https://github.com/raywenderlich/swift-algorithm-club/tree/master/Segment%20Tree/LazyPropagation)
- kd-Tree
- [Heap](Heap/). A binary tree stored in an array, so it doesn't use pointers. Makes a great priority queue.
- Fibonacci Heap
- [Trie](Trie/). A special type of tree used to store associative data structures.
- [B-Tree](B-Tree/). A self-balancing search tree, in which nodes can have more than two children.
- [QuadTree](QuadTree/). A tree with 4 children.
- [Octree](Octree/). A tree with 8 children.

### Hashing

- [Hash Table](Hash%20Table/). Allows you to store and retrieve objects by a key. This is how the dictionary type is usually implemented.
- Hash Functions

### Sets

- [Bloom Filter](Bloom%20Filter/). A constant-memory data structure that probabilistically tests whether an element is in a set.
- [Hash Set](Hash%20Set/). A set implemented using a hash table.
- [Multiset](Multiset/). A set where the number of times an element is added matters. (Also known as a bag.)
- [Ordered Set](Ordered%20Set/). A set where the order of items matters.

### Graphs

- [Graph](Graph/)
- [Breadth-First Search (BFS)](Breadth-First%20Search/)
- [Depth-First Search (DFS)](Depth-First%20Search/)
- [Shortest Path](Shortest%20Path%20%28Unweighted%29/) on an unweighted tree
- [Single-Source Shortest Paths](Single-Source%20Shortest%20Paths%20(Weighted)/)
- [Minimum Spanning Tree](Minimum%20Spanning%20Tree%20%28Unweighted%29/) on an unweighted tree
- [Minimum Spanning Tree](Minimum%20Spanning%20Tree/)
- [All-Pairs Shortest Paths](All-Pairs%20Shortest%20Paths/)
- [Dijkstra's shortest path algorithm](Dijkstra%20Algorithm/)

## Puzzles

A lot of software developer interview questions consist of algorithmic puzzles. Here is a small selection of fun ones. For more puzzles (with answers), see [here](http://elementsofprogramminginterviews.com/) and [here](http://www.crackingthecodinginterview.com).

- [Two-Sum Problem](Two-Sum%20Problem/)
- [Three-Sum/Four-Sum Problem](3Sum%20and%204Sum/)
- [Fizz Buzz](Fizz%20Buzz/)
- [Monty Hall Problem](Monty%20Hall%20Problem/)
- [Finding Palindromes](Palindromes/)
- [Dining Philosophers](DiningPhilosophers/)
- [Egg Drop Problem](Egg%20Drop%20Problem/)
## Learn more!

For more information, check out these great books:

- [Introduction to Algorithms](https://mitpress.mit.edu/books/introduction-algorithms) by Cormen, Leiserson, Rivest, Stein
- [The Algorithm Design Manual](http://www.algorist.com) by Skiena
- [Elements of Programming Interviews](http://elementsofprogramminginterviews.com) by Aziz, Lee, Prakash
- [Algorithms](http://www.cs.princeton.edu/~rs/) by Sedgewick
- [Grokking Algorithms](https://www.manning.com/books/grokking-algorithms) by Aditya Bhargava

The following books are available for free online:

- [Algorithms](http://www.beust.com/algorithms.pdf) by Dasgupta, Papadimitriou, Vazirani
- [Algorithms, Etc.](http://jeffe.cs.illinois.edu/teaching/algorithms/) by Erickson
- [Algorithms + Data Structures = Programs](http://www.ethoberon.ethz.ch/WirthPubl/AD.pdf) by Wirth
- Algorithms and Data Structures: The Basic Toolbox by Mehlhorn and Sanders
- [Open Data Structures](http://opendatastructures.org) by Pat Morin
- [Wikibooks: Algorithms and Implementations](https://en.wikibooks.org/wiki/Algorithm_Implementation)

Other algorithm repositories:

- [EKAlgorithms](https://github.com/EvgenyKarkan/EKAlgorithms). A great collection of algorithms in Objective-C.
- [@lorentey](https://github.com/lorentey/). Production-quality Swift implementations of common algorithms and data structures.
- [Rosetta Code](http://rosettacode.org). Implementations in pretty much any language you can think of.
- [AlgorithmVisualizer](http://jasonpark.me/AlgorithmVisualizer/). Visualize algorithms on your browser.
- [Swift Structures](https://github.com/waynewbishop/SwiftStructures) Data Structures with directions on how to use them [here](http://waynewbishop.com/swift)

## Credits

The Swift Algorithm Club was originally created by [Matthijs Hollemans](https://github.com/hollance).

It is now maintained by [Vincent Ngo](https://www.raywenderlich.com/u/jomoka), [Kelvin Lau](https://github.com/kelvinlauKL) and [Ross O'brien](https://www.raywenderlich.com/u/narrativium).

The Swift Algorithm Club is a collaborative effort from the [most algorithmic members](https://github.com/rwenderlich/swift-algorithm-club/graphs/contributors) of the [raywenderlich.com](https://www.raywenderlich.com) community. We're always looking for help - why not [join the club](.github/CONTRIBUTING.md)? :]

## License

All content is licensed under the terms of the MIT open source license.

By posting here, or by submitting any pull request through this forum, you agree that all content you submit or create, both code and text, is subject to this license.  Razeware, LLC, and others will have all the rights described in the license regarding this content.  The precise terms of this license may be found [here](https://github.com/raywenderlich/swift-algorithm-club/blob/master/LICENSE.txt).

[![Build Status](https://travis-ci.org/raywenderlich/swift-algorithm-club.svg?branch=master)](https://travis-ci.org/raywenderlich/swift-algorithm-club)


