# Is Characters In A String Unique?

**Question (CTCI 1.1)**

Given a string, create an algorithm to test whether all characters in the string are unique.

**Intuition**

**Solution 1**
O(n) O(n). Use a dictionary
```python
def unique_charaters(string): 
    seen = {}
    for char in string:
        if char in seen:
            return False
        seen[char] = 0
    return True
```
**Solution 2**
```python
def unique_charaters(string):
    '''O(nlogn) O(n). This does not use any data structures. sorted() return new list'''
    sorted_string = sorted(string)
    for i in range(1, len(string)):
        if sorted_string[i] == sorted_string[i-1]:
            return False
    return True
```
**Solution 3**
```python
def unique_charaters(string): #O(n2) O(1). This solution does not require extra space with a time tradeoff
    for i in range(len(string)):
        for j in range(len(string)):
            if i == j:
                continue
            if string[i] == string[j]:
                return False
    return True

```