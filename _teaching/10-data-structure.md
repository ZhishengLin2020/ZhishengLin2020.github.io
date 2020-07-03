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

## 1. Algorithms

### 1.1 Basis

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

### 1.2 Search Algorithms

#### Linear Search
- Principle: Pick out each element in that list and compare it with the target value. Search from beginning to end.
```python
def liner_search(li, val):
	for ind, v in enumerate(li):
		if v == val:
			return ind
	else:
		return None
```
- Time Complexity: $\mathcal{O}(n)$

#### Binary Search
- Principle: First, the list is about to be searched should be a sorthed list. Then, compare the target value with the mid value in the list and narrow the target area down.<br/>
<img src='/images/linear_search.gif' width='500' height='300'>
```python
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
```
- Time Complexity: $\mathcal{O}(\log_2 n)$

#### Comparision
Although the binary search is faster than linear search, binary needs to sort the list at the beginning, which has $\mathcal{O}(n)$ time complexity and make it slower.

### 1.3 Sort Algorithms

#### 1.3.1 Slow Sort Algorithms

##### Bubble Sort
- Principle: Compare each 2 adjacent element. If the one in front is larger than the one in behind, swap them. At the end of each loop, the disordered area decreases 1 element and the ordered area increases 1 element.<br/>
<img src='/images/bubble_sort.gif' width='300' height='500'>
```python
def bubble_sort(li):
	for i in range(len(li)-1): # ith loop
		exchange = False
		for j in range(len(li)-i-1):
			if li[j] > li[j+1]:
				li[j], li[j+1] = li[j+1], li[j]
				exchange = True
		if not exchange:
			return
```
- Time Complexity: $\mathcal{O}(n^2)$

##### Select Sort
- Principle: See list as two area, one is ordered area, the other one is disordered area. Select the first element in disordered area and compare it with other elements in the disordered area. If the smaller element is found, swapping the first element in the disordered area with the smaller element.<br/>\
```python
def select_sort(li):
	

```



##### Insert Sort

#### 1.3.2 Fast Sort Algorithms

##### Quick Sort

##### Stack Sort

##### Merge Sort

#### 1.3.3 Other Sort Algorithms

##### Shell Sort

##### Count Sort

##### Bucket Sort

##### Radix Sort






















