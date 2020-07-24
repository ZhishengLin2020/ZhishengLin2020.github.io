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

```python
def insertLast(self, value: int) -> bool:
	"""
	Adds an item at the rear of Deque. Return true if the operation is successful.
	"""
	if self.cur_n == self.max_n:  # 队满
		return False
	self.queue[self.rear] = value
	self.rear = (self.rear + 1) % self.max_n
	self.cur_n += 1
	return True
```














