## Merge Sort
Overview

Merge Sort is a divide-and-conquer sorting algorithm that recursively divides the array into smaller subarrays until each subarray contains a single element. These subarrays are then merged back together in sorted order.

Time Complexity

Best Case: O(n log n)

Average Case: O(n log n)

Worst Case: O(n log n)

📌 The time complexity remains the same in all cases because the array is always divided into two halves.

Space Complexity

O(n)
❌ Not in-place
❌ Requires additional memory for merging

Complexity Analysis (Recursion Tree / Master Method)

Recurrence relation:

T(n) = 2T(n / 2) + n


Cost at each level = n

Number of levels = log n

Using Recursion Tree Method:

T(n) = Θ(n log n)


Using Master Method:

a = 2, b = 2, f(n) = n

Case 2 applies

T(n) = Θ(n log n)

## Quick Sort
Overview

Quick Sort is a divide-and-conquer algorithm that selects a pivot element and partitions the array such that elements smaller than the pivot are placed on one side and larger elements on the other. The process is then applied recursively to the subarrays.

Time Complexity

Best Case: O(n log n)

Average Case: O(n log n)

Worst Case: O(n²)

📌 The worst case occurs when the pivot selection results in highly unbalanced partitions.

Space Complexity

O(log n) (Average Case)
✔ In-place (except recursion stack)

Complexity Analysis (Recursion Tree)

Best / Average Case:
Balanced partitioning leads to:

log n levels × n work per level = O(n log n)


Worst Case:
Unbalanced partitioning results in:

n levels × n work = O(n²)


❌ Master Method does not apply cleanly due to uneven subproblem sizes.

## Heap Sort
Overview

Heap Sort is a comparison-based sorting algorithm that uses a binary heap data structure. The array is first converted into a max heap, and then the largest element is repeatedly removed and placed at the end of the array.

Time Complexity

Best Case: O(n log n)

Average Case: O(n log n)

Worst Case: O(n log n)

📌 Performance is consistent regardless of input order.

Space Complexity

O(1)
✔ In-place
✔ No additional memory required

Complexity Analysis

Building the heap: O(n)

Heapify operation repeated n times, each costing O(log n)

Total complexity:

O(n log n)


❌ Not recursive in the traditional sense
❌ Recursion Tree and Master Method are not applicable

Final Comparison (All Algorithms)

Algorithm	Best Case	Average Case	Worst Case	Space	In-Place

Bubble Sort	O(n)	O(n²)	O(n²)	O(1)	✔

Selection Sort	O(n²)	O(n²)	O(n²)	O(1)	✔

Insertion Sort	O(n)	O(n²)	O(n²)	O(1)	✔

Merge Sort	O(n log n)	O(n log n)	O(n log n)	O(n)	❌

Quick Sort	O(n log n)	O(n log n)	O(n²)	O(log n)	✔

Heap Sort	O(n log n)	O(n log n)	O(n log n)	O(1)	✔

Overall Conclusion

Divide-and-conquer sorting algorithms such as Merge Sort, Quick Sort, and Heap Sort significantly outperform simple quadratic sorting algorithms on large datasets. While Merge Sort guarantees optimal time complexity, it requires additional memory. Quick Sort offers excellent average-case performance, and Heap Sort provides consistent performance with minimal memory usage.
