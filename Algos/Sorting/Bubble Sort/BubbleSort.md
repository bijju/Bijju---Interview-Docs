# **Bubble Sort**
Bubble sort, sometimes referred to as sinking sort, is a simple sorting algorithm that repeatedly steps through the list to be sorted, compares each pair of adjacent items and swaps them if they are in the wrong order. The pass through the list is repeated until no swaps are needed, which indicates that the list is sorted. The algorithm, which is a comparison sort, is named for the way smaller or larger elements "bubble" to the top of the list. Although the algorithm is simple, it is too slow and impractical for most problems even when compared to insertion sort.[2] Bubble sort can be practical if the input is in mostly sorted order with some out-of-order elements nearly in position.

## **Big O Analysis**
* Nested Loops
* O(n^2)
* Best for small datasets

## **Example**
**Note: **
Idea is to start from left most item to identify max item and compare to adjacent items (oin right) until sort items are accumulated on right!

5 8 1 6 9 2  
* Iteration 1:   
  * **5** **8** 1 6 9 2   
  * 5 **8** **1** 6 9 2 -> Swap  
  * 5 1 **8** **6** 9 2 -> Swap  
  * 5 1 6 **8** **9** 2 -> Nothing, move to next number  
  * 5 1 6 8 **9** **2** -> Swap  
  * 5 1 6 8 2 **[9]** -> Right most item is sorted    
* Iteration 2*
  * **5** **1** 6 8 2 **[9]** -> Swap  
  * 1 **5** **6** 8 2 **[9]** -> Nothing, move to next item  
  * 1 5 **6** **8** 2 **[9]** -> Nothing, move to next item
  * 1 5 6 **8** **2** **[9]** -> swaps
  * 1 5 6 2 **[8 9]** -> Right most item is sorted  
* Iteration 3:
  * **1** **5** 6 2 **[8 9]** -> Move to next item
  * 1 **5** **6** 2 **[8 9]** -> Move to next item  
  * 1 5 **6** **2** **[8 9]** -> Swap
  * 1 5 2 **[6 8 9]** -> Right most item is sorted  
* Iteration 4:
  * **1** **5** 2 **[6 8 9]** -> Next
  * 1 **5** **2** **[6 8 9]** -> swaps
  1 2 **[5 6 8 9]**
* Iteration 5:
  * **1** **2** **[5 6 8 9]** -> Next  
  * **[1 2 5 6 8 9]** -> **Done!**
