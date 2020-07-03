---
title: "Data Structures"
collection: courses
type: "Undergraduate course"
permalink: /courses/data-structures
venue: "University of California Berkeley, Electrical Engineering and Computer Sciences"
date: 2020-06-01
# location: "City, Country"
---

Master some fundamental dynamic data structures, including linear lists, queues, trees, and other linked structures; arrays strings, and hash tables. Storage management. Elementary principles of software engineering. Abstract data types. Algorithms for sorting and searching. Introduction to the Java programming language.

## Algorithms

### Basis

#### Time Complexity
- $\mathcal{O}(1)$: Command lines are few
- $\mathcal{O}(\log_2 n)$: Have loops that reducing half of the data each time
- $\mathcal{O}(n^2)$: Have 2 **nested** loops
- Be careful: 
	- algorithms with recursion would need graph to have a better understanding
	- algorithms would have best/ordinary/worst condition

#### Space Complexity
- $\mathcal{O}(1)$: Variables created are few, which can be counted
- $\mathcal{O}(n)$: 1D **list/array** with n elements
- $\mathcal{O}(mn)$: 2D **list/array** with m$\times$n elements

#### Recursion
- What is the end condition
- What is the return value
- What should be done in each recursion

### Search Algorithms
#### Linear Search
- Principle: Pick out each element in that list and compare it with the target value. Search from beginning to end.
<pre>
<font size = 7>
def liner_search(li, val):
	for ind, v in enumerate(li):
		if v == val:
			return ind
	else:
		return None
</pre>
- Time Complexity: $\mathcal{O}(n)$

#### Binary Search
- Principle: First, the list is about to be searched should be a sorthed list. Then, compare the target value with the mid value in the list and narrow the target area down.<br/>
<img src='/images/linear_search.gif' width='500' height='300'>
<pre>
<font size = 7>
def binary_search(li, val):
	left = 0
	right = len(li)-1
	while left <= right:
		mid = (mid + right) // 2
		if li[mid] == val:
			return mid
		elif li[mid] > val:
			right = mid - 1
		else:
			left = mid + 1
	else:
		return None
</pre>
- Time Complexity: $\mathcal{O}(\log_2 n)$

#### Comparision
Although the binary search is faster than linear search, binary needs to sort the list at the beginning, which has $\mathcal{O}(n)$ time complexity and make it slower.

### Sort Algorithms

#### Slow Sort Algorithms


#### Fast Sort Algorithms


#### Other Sort Algorithms






















