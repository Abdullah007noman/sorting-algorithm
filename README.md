# sorting-algorithm
This repository contains implementations of three fundamental sorting algorithms:

-Bubble Sort

-Insertion Sort

-Selection Sort

Each algorithm is implemented in Python and is accompanied by a brief explanation of how it works.
## 1. Insertion Sort
Description:
Insertion Sort builds the final sorted array one element at a time. It takes each element from the input and inserts it into its correct position in the already-sorted part of the array.

## Time Complexity <br />
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
```

## 2.Selection Sort
Description:
Selection Sort works by repeatedly selecting the smallest (or largest, depending on the order) element from the unsorted portion of the list and swapping it with the first unsorted element. This process continues until the entire list is sorted.

## Time Complexity <br />
Worst-case: O(n²)

Best-case: O(n²)

Average-case: O(n²)
## Usage
``` python
def selection_sort(arr):
    for i in range(len(arr)):
        min_idx = i
        for j in range(i+1, len(arr)):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]
    return arr
```
## Correctness of Selection Sort
Selection Sort is correct because it maintains the following loop invariant:

At the start of each iteration of the outer loop, the subarray arr[0..i-1] is sorted and contains the smallest i elements of the array.

* Initialization: Before the first iteration (i = 0), the subarray arr[0..-1] is empty and trivially sorted.

* Maintenance: During each iteration, the algorithm finds the smallest element in the unsorted portion of the array (arr[i..n-1]) and swaps it with arr[i]. This ensures that arr[i] is now in its correct position in the sorted portion of the array.

* Termination: When the outer loop completes (i = n-1), the subarray arr[0..n-2] is sorted, and the last element arr[n-1] is already in its correct position. Thus, the entire array is sorted.

Since the loop invariant holds before the loop starts, after each iteration, and upon termination, Selection Sort correctly sorts the input array.


## 3.Bubble Sort
Description:
Bubble Sort is a simple comparison-based sorting algorithm. It repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. This process is repeated until the list is sorted.

## Time Complexity<br />
Worst-case: O(n²)

Best-case: O(n) (when the list is already sorted)

Average-case: O(n²)

## Usage

``` python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr

```

## How to Use
* Clone the Repository:
``` bash
git clone https://github.com/your-username/sorting-algorithms.git
```
* Navigate to the repository:
``` bash
cd sorting-algorithms
```
* Open the Jupyter Notebook:

If you have Jupyter installed, run:

```bash
jupyter notebook
```
This will open the Jupyter interface in your browser. Navigate to the .ipynb file and open it.

* Run the cells in the notebook:

Each sorting algorithm is implemented in its own cell. You can run the cells individually to see how the algorithms work.

To run a cell, select it and press Shift + Enter.








