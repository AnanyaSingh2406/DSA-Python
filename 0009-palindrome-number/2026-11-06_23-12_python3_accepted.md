# 9. Palindrome Number
  
<br>**Problem:** https://leetcode.com/problems/palindrome-number/<br>

**Difficulty:** Easy<br>
**Topics:** Math<br>
**Language:** python3<br>
**Status:** Accepted<br>
**Submitted:** 2026-11-06 23:12 local time

**Runtime:** 16 ms (beats 23.093399999999985%)
**Memory:** 19.2 MB (beats 77.51520000000002%)


<!-- leetgit:submissionId=2190866581 codeHash=1490f3f515bd5634e7914036bc6f5af73cca6b52396912d59a02e8d00f80a5ab notesHash=e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855 -->

## Solution

```python3
#Palindrome
class Solution:
    def isPalindrome(self, x: int) -> bool:
        a = str(x)
        b = a[::-1]
        if a==b :
            return True
        else:
            return False
        
```
