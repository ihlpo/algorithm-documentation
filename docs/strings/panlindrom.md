# Panlindom

Create a function that will test whether a given string is a panlindom

```python
def test_palindromicity(string):
    forward  = 0
    backward = len(string) - 1

    while forward < backward:
        while not string[forward].isalnum() and forward < backward:
            forward += 1
        while not string[backward].isalnum() and forward < backward:
            backward -=1
        if string[forward].lower() != string[backward].lower():
            return False
        forward += 1
        backward -= 1
    return True
```