Non-Comparison Sorting Algorithms

Unlike comparison-based sorting algorithms, non-comparison sorting algorithms do not rely on comparing elements directly. As a result, they can achieve linear time complexity under specific constraints, at the cost of additional memory usage and restricted input types.

## Counting Sort
Overview

Counting Sort is a non-comparison sorting algorithm that sorts elements by counting the number of occurrences of each distinct value. The algorithm uses these counts to determine the correct position of each element in the output array.

📌 Applicable only to non-negative integers with a limited range.

Time Complexity

Best Case: O(n + k)

Average Case: O(n + k)

Worst Case: O(n + k)

Where:

n = number of elements

k = range of input values

Space Complexity

O(n + k)
❌ Not in-place
❌ Requires additional memory proportional to the input range

Complexity Analysis

One pass to count occurrences → O(n)

One pass over the range of values → O(k)

Total complexity:

O(n + k)


❌ Not recursive
❌ Master Method and Recursion Tree Method do not apply

## Radix Sort
Overview

Radix Sort sorts numbers digit by digit, starting from the least significant digit to the most significant digit. It typically uses Counting Sort as a stable subroutine for sorting at each digit position.

📌 Suitable for integers or fixed-length strings.

Time Complexity

Best Case: O(d × (n + k))

Average Case: O(d × (n + k))

Worst Case: O(d × (n + k))

Where:

d = number of digits

k = base of the number system (commonly 10)

In practice:

O(d × n)

Space Complexity

O(n + k)
❌ Not in-place
❌ Requires auxiliary arrays

Complexity Analysis

Counting Sort is applied d times

Each pass costs O(n + k)

Total complexity:

O(d × (n + k))


❌ Not recursive
❌ Master Method and Recursion Tree Method do not apply

## Bucket Sort
Overview

Bucket Sort divides the input elements into a number of buckets, sorts each bucket individually, and then concatenates all buckets to produce the final sorted array. It performs best when the input data is uniformly distributed.

📌 Commonly used for floating-point numbers.

Time Complexity

Best Case: O(n)

Average Case: O(n)

Worst Case: O(n²)

📌 The worst case occurs when all elements fall into a single bucket.

Space Complexity

O(n)
❌ Not in-place
❌ Requires additional memory for buckets

Complexity Analysis

Uniform distribution → small bucket sizes

Sorting within buckets is efficient

Average case complexity:

O(n)


❌ Not recursive
❌ Master Method and Recursion Tree Method do not apply

Summary: Non-Comparison Sorting

Algorithm	Best Case	Average Case	Worst Case	Space	In-Place

Counting Sort	O(n + k)	O(n + k)	O(n + k)	O(n + k)	❌

Radix Sort	O(d·n)	O(d·n)	O(d·n)	O(n + k)	❌

Bucket Sort	O(n)	O(n)	O(n²)	O(n)	❌

Final Remarks

Non-comparison sorting algorithms can outperform comparison-based algorithms by achieving linear time complexity. However, this performance comes with trade-offs, including increased memory usage and strict assumptions about the input data.
