# sorting-algorithm
This repository contains implementations of three fundamental sorting algorithms:

-Bubble Sort

-Insertion Sort

-Selection Sort

Each algorithm is implemented in Python and is accompanied by a brief explanation of how it works.
## 1. Insertion Sort
Description:
Insertion Sort builds the final sorted array one element at a time. It takes each element from the input and inserts it into its correct position in the already-sorted part of the array.

Time Complexity:
Worst-case: O(n²)

Best-case: O(n) (when the list is already sorted)

Average-case: O(n²)
## Usage
``` python
def insertion_sort(arr):
    for i in range(1, len(arr)):
        key = arr[i]
        j = i - 1
        while j >= 0 and key < arr[j]:
            arr[j + 1] = arr[j]
            j -= 1
        arr[j + 1] = key
    return arr

## 2.Selection Sort
Description
Selection Sort works by repeatedly selecting the smallest (or largest, depending on the order) element from the unsorted portion of the list and swapping it with the first unsorted element. This process continues until the entire list is sorted.

Time Complexity
Worst-case: O(n²)

Best-case: O(n²)

Average-case: O(n²)
