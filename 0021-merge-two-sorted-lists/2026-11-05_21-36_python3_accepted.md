# 21. Merge Two Sorted Lists
  
<br>**Problem:** https://leetcode.com/problems/merge-two-sorted-lists/<br>

**Difficulty:** Easy<br>
**Topics:** Linked List, Recursion<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-05 21:36 local time

**Runtime:** 0 ms (beats 100%)
**Memory:** 19.1 MB (beats 95.9272%)


<!-- leetgit:submissionId=2190183811 codeHash=439ab1035f8c7210ed7ec2e355e6fbe5560414d31c78b064cc5cd27e3700e56f notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
#test sync

class Solution:
    def mergeTwoLists(self, list1: Optional[ListNode], list2: Optional[ListNode]) -> Optional[ListNode]:
        # Create a dummy node to hold the start of the merged list
        dummy = ListNode(-1)
        current = dummy
        
        # Traverse both lists while they both have nodes
        while list1 and list2:
            if list1.val <= list2.val:
                current.next = list1
                list1 = list1.next
            else:
                current.next = list2
                list2 = list2.next
            current = current.next
            
        # Append the remaining nodes from whichever list is not empty
        current.next = list1 if list1 else list2
        
        # The head of the merged list is the next node after the dummy
        return dummy.next
```
