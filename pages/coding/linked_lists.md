---
layout: page
title: Linked Lists
permalink: /pages/coding/linked_lists
---

### Notes

* The head element of a singly linked list should always be tracked or else it will be garbage collected.
* In order to solve singly-linked list problems it's best to take into account these three pointers/references: `prev`, `current` and `next`. It will simplify the code a lot and is easy to navigate visually.
  
### Basics

```python
# Definition for singly-linked list.
class ListNode(object):
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next
```

### Reverse a linked list

```python
class Solution(object):
    def reverseList(self, head):
        prev = None
        current = head
        while current != None:
            next = current.next
            current.next = prev     # main operation in this code
            prev = current
            current = next
        return prev
```

Practice: [leetcode](https://leetcode.com/problems/reverse-linked-list/)