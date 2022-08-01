# The Dutch National Flag Problem

**Question**
Write a program that takes an array A and an index i into A
```python
    def national_flag(array, index):
        array1 = []
        for i in array:
            if i < array[index]:
                array1.append(i)

        for i in array:
            if i == array[index]:
                array1.append(i)

        for i in array:
            if i > array[index]:
                array1.append(i)

        return array1
```