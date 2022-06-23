# What is it?
QuickSort is a divide and conquer algorithm. It picks an element as a pivot and partitions the given array around the picked pivot. There are many different versions of quickSort that pick pivot in different ways.   
1.Always pick the first element as a pivot.    
2.Always pick the last element as a pivot.  
3.Pick a random element as a pivot.  
4.Pick median as a pivot.  


Code Example:

```python
def quicksort(arr):
    qs(arr, 0, len(arr) - 1)

def qs(arr, l, r):
    if l >= r:
        return
    p = partition(arr, l, r)

    qs(arr, l, p - 1)
    qs(arr, p + 1, r)

def partition(arr, l, r):
    pivot = arr[r]
    i = l - 1
    for j in range(l, r):
        if arr[j] < pivot:
            i += 1
            arr[i], arr[j] = arr[j], arr[i]
    arr[i + 1], arr[r] = arr[r], arr[i + 1]
    return i + 1
'''
a1 = [3, 2, 1]
a2 = [1, 2, 3]
a3 = []
a4 = [3, 1, -1, 0, 2, 5]
a5 = [2, 2, 1, 1, 0, 0, 4, 4, 2, 2, 2]
a6 = [0]
a7 = [3, -2, -1, 0, 2, 4, 1]
a8 = [1, 2, 3, 4, 5, 6, 7]
a9 = [2, 2, 2, 2, 2, 2, 2]

quicksort(a1)
quicksort(a2)
quicksort(a3)
quicksort(a4)
quicksort(a5)
quicksort(a6)
quicksort(a7)
quicksort(a8)
quicksort(a9)

assert a1 == [1, 2, 3]
assert a2 == [1, 2, 3]
assert a3 == []
assert a4 == [-1, 0, 1, 2, 3, 5]
assert a5 == [0, 0, 1, 1, 2, 2, 2, 2, 2, 4, 4]
assert a6 == [0]
assert a7 == [-2, -1, 0, 1, 2, 3, 4]
assert a8 == [1, 2, 3, 4, 5, 6, 7]
assert a9 == [2, 2, 2, 2, 2, 2, 2]

print("If you didn't get an assertion error, this program has run successfully.")
```
