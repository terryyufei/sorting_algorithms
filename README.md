# 0x1B. C - Sorting algorithms & Big O

## Quick Sort
* QuickSort is a widely used sorting algorithm that follows the divide-and-conquer approach. It is known for its       efficiency and typically outperforms other sorting algorithms, such as Bubble Sort or Insertion Sort, especially when * dealing with large datasets.

* The basic idea behind QuickSort is to select a pivot element from the array and partition the other elements into two sub-arrays based on whether they are less than or greater than the pivot. The sub-arrays are then recursively sorted using the same process until the entire array is sorted.

### Here's a step-by-step explanation of the QuickSort algorithm:
* Choose a pivot: Select an element from the array to serve as the pivot. The choice of the pivot can affect the performance of the algorithm, but a common approach is to select the last element of the array.

* Partitioning: Rearrange the array in such a way that all elements less than the pivot are moved to the left side of the pivot, and all elements greater than the pivot are moved to the right side. The pivot itself will be in its final sorted position.

* Recursion: Recursively apply the above two steps to the sub-arrays on the left and right sides of the pivot. This process continues until each sub-array contains only one element, at which point the array is considered sorted.

* Combining the sub-arrays: As the recursion unwinds, the sub-arrays are combined back to obtain the final sorted array.

* The partitioning step is crucial in QuickSort, as it determines the position of the pivot and separates the elements smaller and larger than the pivot. One popular approach is the Lomuto partition scheme, which works as follows:

* Initialize two pointers, i and j, where i points to the first element and j iterates through the remaining elements.

* Starting from the first element, compare each element with the pivot. If the element is smaller than the pivot, swap it with the element at i and increment i.

* Continue this process until j reaches the end of the array.

* Finally, swap the pivot (which is currently at the last position) with the element at index i.

* After the partitioning step, the pivot is in its correct position, and all elements to its left are smaller, while all elements to its right are greater.

* The time complexity of QuickSort is typically expressed in terms of Big O notation, and in the average case, it has a time complexity of O(n log n), where 'n' is the number of elements in the array. However, in the worst case, QuickSort's time complexity can degrade to O(n^2), which occurs when the chosen pivot consistently partitions the array into highly imbalanced sub-arrays. Nevertheless, various optimizations, like choosing a random pivot or implementing the three-way partitioning scheme, can mitigate this issue and make QuickSort perform well in practice.