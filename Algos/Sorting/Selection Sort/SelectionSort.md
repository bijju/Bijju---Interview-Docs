# **Selection Sort**
selection sort is a sorting algorithm, specifically an in-place comparison sort. It has O(n2) time complexity, making it inefficient on large lists, and generally performs worse than the similar insertion sort. Selection sort is noted for its simplicity, and it has performance advantages over more complicated algorithms in certain situations, particularly where auxiliary memory is limited.

The algorithm divides the input list into two parts: the sublist of items already sorted, which is built up from left to right at the front (left) of the list, and the sublist of items remaining to be sorted that occupy the rest of the list. Initially, the sorted sublist is empty and the unsorted sublist is the entire input list. The algorithm proceeds by finding the smallest (or largest, depending on sorting order) element in the unsorted sublist, exchanging (swapping) it with the leftmost unsorted element (putting it in sorted order), and moving the sublist boundaries one element to the right.


## **Big O Analysis**
* Not fast since it uses Nested Loops to sort
* O(n^2)
* Good for small list of items


## **Example**
7 8 5 4 9 2    -> **Find smallest item, and swap wih left most unsorted value!**  
**Min Value** = 7 > 5 > 4 > 2 = **2**  

* **[ _ _ _ _ _ _ ]** <<  **7** 8 5 4 9 **2** -> Min Number: 2 (Swap 2 with left most unsorted number: 7)   
* **[ 2 _ _ _ _ _ ]** << **8** 5 **4** 9 7 -> Min Value = 8 > 5 > 4 (Swap 4 with left most unsorted number: 8)     
* **[ 2 4 _ _ _ _ ]** << **5** 8 9 7 -> Min Number: 5  (Set 5 as sorted)
* **[ 2 4 5 _ _ _ ]** << **8** 9 **7** -> Min Number: 7 (Swap 7 with left most unsorted number: 8)  
* **[ 2 4 5 7 _ _ ]** << **9** **8** -> Min Number: 8 (Swap 8 with left most unsorted number: 9)  
* **[ 2 4 5 7 8 9 ]** << **Done!**    
