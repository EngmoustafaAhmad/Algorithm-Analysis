# Comparison-Based Sorting Algorithms

This document provides an analytical overview of three fundamental comparison-based sorting algorithms: Bubble Sort, Selection Sort, and Insertion Sort.
Each algorithm is evaluated in terms of time complexity, space complexity, and computational behavior.

## Bubble Sort
Overview

Bubble Sort is a simple comparison-based sorting algorithm that repeatedly compares adjacent elements and swaps them if they are in the wrong order. After each pass, the largest element moves to its correct position at the end of the array, similar to a bubble rising to the surface.

Time Complexity

Best Case:
O(n)
Occurs when the array is already sorted. Only one pass is required to confirm the order.

Average Case:
O(n²)
Caused by repeated comparisons between adjacent elements.

Worst Case:
O(n²)
Occurs when the array is sorted in reverse order, resulting in the maximum number of swaps.

Space Complexity

O(1)
✔ In-place algorithm
✔ Does not require additional memory

Complexity Analysis

The algorithm uses two nested loops

The number of operations grows proportionally to:

n × n


❌ Not recursive
❌ Cannot be analyzed using:

Master Method

Recursion Tree Method

## Selection Sort
Overview

Selection Sort works by repeatedly selecting the smallest element from the unsorted portion of the array and placing it at the correct position. This process continues until the entire array is sorted.

Time Complexity

Best Case: O(n²)

Average Case: O(n²)

Worst Case: O(n²)

📌 The number of comparisons remains constant regardless of the initial order of the input data.

Space Complexity

O(1)
✔ In-place algorithm
✔ Requires no extra memory

Complexity Analysis

Uses two nested loops:

Outer loop to select the position

Inner loop to find the minimum element

Total number of comparisons:

n(n − 1) / 2


❌ Not recursive
❌ Recursion Tree and Master Method are not applicable

## Insertion Sort
Overview

Insertion Sort follows the same principle as sorting playing cards. Each element is inserted into its correct position within the already sorted portion of the array.

Time Complexity

Best Case:
O(n)
Occurs when the array is already sorted.

Average Case:
O(n²)

Worst Case:
O(n²)
Occurs when the array is sorted in reverse order.

Space Complexity

O(1)
✔ Memory-efficient
✔ In-place algorithm

Complexity Analysis

In the worst case:

Each element may need to be shifted across most of the array

Total number of operations:

1 + 2 + 3 + ... + n = O(n²)


❌ Not recursive
❌ Master Method and Recursion Tree Method do not apply

## Summary Comparison

Algorithm	     |  Best  | Case	|   Average	| Case Worst Case		| Space	In-Place.

Bubble Sort    |	O(n)	| O(n²)	|   O(n²)		|   O(1)		|  ✔

Selection Sort |  O(n²)	| O(n²)	| 	O(n²)		|   O(1)		|  ✔

Insertion Sort |  O(n)	| O(n²)	| 	O(n²)		|   O(1)		|  ✔
