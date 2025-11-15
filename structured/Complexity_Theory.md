When we talk about complexity levels in computer science, we usually mean time complexity and space complexity—how the resources (time or memory) required by an algorithm grow as the input size grows. Here’s a structured list of the common ones, ordered roughly from fastest/smallest to slowest/largest:


---

1. Constant Time – O(1)

Resource usage does not grow with input size.

Example: Accessing an element in an array by index, checking if a number is even.

Very efficient and ideal.



---

2. Logarithmic Time – O(log n)

Resource usage grows slowly, proportional to the logarithm of the input size.

Example: Binary search, balanced BST search (like AVL or Red-Black Tree), some divide-and-conquer algorithms.

Doubling the input size increases steps only slightly.



---

3. Linear Time – O(n)

Resource usage grows directly with input size.

Example: Iterating through an array, finding max/min in a list.

Simple and common.



---

4. Linearithmic Time – O(n log n)

Grows faster than linear but slower than quadratic.

Example: Efficient sorting algorithms (merge sort, heap sort, quicksort average case), some divide-and-conquer algorithms.



---

5. Quadratic Time – O(n²)

Resource usage grows proportional to the square of the input size.

Example: Bubble sort, insertion sort, naive matrix multiplication.

Fine for small inputs, but quickly becomes slow.



---

6. Cubic Time – O(n³)

Resource usage grows with the cube of the input size.

Example: Some dynamic programming algorithms (like naive Floyd-Warshall for all-pairs shortest path), triple nested loops.

Often impractical for large inputs.



---

7. Polynomial Time – O(n^k)

Generalization of quadratic/cubic: grows as n to some constant power k.

Example: Many combinatorial algorithms with k nested loops.

Acceptable for small n, but scales poorly.



---

8. Exponential Time – O(2^n)

Resource usage doubles with each additional input element.

Example: Brute-force subset generation, traveling salesman naive solution.

Very slow; feasible only for small inputs.



---

9. Factorial Time – O(n!)

Resource usage grows as factorial of input size.

Example: Generating all permutations of n elements, brute-force TSP.

Practically unusable for n > 10–15.



---

10. Sub-linear Time – O(√n), O(log n), O(log log n)

Time grows slower than linear, often in algorithms that sample or skip parts of data.

Example: Jump search (O(√n)), binary search (O(log n)).



---

11. Space Complexity Variants

Often parallels time complexity:

O(1): Constant extra memory

O(n): Memory grows linearly with input

O(n²), O(2^n), etc., same as time complexity patterns


Important for algorithms with large datasets or embedded systems.



---

Big-O Hierarchy (from fastest to slowest)

O(1) < O(log n) < O(n) < O(n log n) < O(n²) < O(n³) < O(n^k) < O(2^n) < O(n!)


---

If you want, I can make a diagram with actual examples of data structures and algorithms at each complexity level, so you can visualize which structures perform best in which scenarios.

Do you want me to do that?