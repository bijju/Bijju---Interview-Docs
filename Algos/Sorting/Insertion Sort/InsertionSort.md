# **Insertion Sort**
Insertion sort is a simple sorting algorithm that builds the final sorted array (or list) one item at a time. It is much less efficient on large lists than more advanced algorithms such as quicksort, heapsort, or merge sort. However, insertion sort provides several advantages:

  * Simple implementation: Jon Bentley shows a three-line C version, and a five-line optimized version[2]
  * Efficient for (quite) small data sets, much like other quadratic sorting algorithms
  * More efficient in practice than most other simple quadratic (i.e., O(n2)) algorithms such as selection sort or bubble sort
  * Adaptive, i.e., efficient for data sets that are already substantially sorted: the time complexity is O(nk) when each element in the input is no more than k places away from its sorted position
  * Stable; i.e., does not change the relative order of elements with equal keys
  * In-place; i.e., only requires a constant amount O(1) of additional memory space
  * Online; i.e., can sort a list as it receives it

## **Big O Analysis:** ##
* Worst case is O(n^2)
* Performance depends on item count (small is better)
* Is not fast sorting algorithm because it uses nested loops to shit items into place.

## **Example** ##
**Note:   **  
Start with index of 1 them compare to left and swap, reset search index to left most unsorted item and compare to sorted items, redo!
* [ 5 8 1 3 9 6 ]
* [ **5** **[8]** 1 3 9 6 ] << is 8 < 5 : False      
* [ 5 **8** **[1]** 3 9 6 ] << is 1 < 8 : True ***[Swap]***  
* [ **5** **[1]** 8 3 9 6 ] << is 1 < 5 : True ***[Swap]***  
* [ **1** 5 8 **[3]** 9 6 ] << Set Index Value to original index position of 1 which is 2 + 1 = 3  
* [ 1 5 **8** **[3]** 9 6 ] << is 3 < 8 : True ***[Swap]***  
* [ 1 **5** **[3]** 8 9 6 ] << is 3 < 5 : True ***[Swap]***  
* [ **1** **[3]** 5 8 9 6 ] << is 3 < 1 : False (Set Search Index to {original index value of 3} 3 + 1 = 4)    
* [ 1 3 5 **8** **[9]** 6 ] << is 9 < 8 : False (Set Search Index tp {original index value of 9's} 4 + 1 = 5)
* [ 1 3 5 8 **9** **[6]** ] << is 6 < 9 : True ***[Swap]***  
* [ 1 3 5 **8** **[6]** 9 ] << is 6 < 8 : True ***[Swap]***  
* [ 1 3 **5** **[6]** 8 9 ] << is 6 < 5 : False  
* **[ 1 3 5 6 8 9 ]** << **Done!**
