# **Quicksort** #

Quicksort (sometimes called partition-exchange sort) is an efficient sorting algorithm, serving as a systematic method for placing the elements of an array in order. Developed by Tony Hoare in 1959[1] and published in 1961,  it is still a commonly used algorithm for sorting. When implemented well, it can be about two or three times faster than its main competitors, merge sort and heapsort.

Since Quicksort is a partition exchange sort, usually is good for large set of items (elements)


## **Big O Analysis:** ##
* Worst case is O(n^2)
* Average case is O(n log n)
* Performance largely depends on Pivot selection


## **Pivot Selection:** ##
Identifying Pivot value decides Performance of quick sort:
* Best pivot value selection to achieve **Optimal Choice: BigO = O(n log n)**
  * `Pivot Value = (int) ((index of first element + index of last element ) / 2)`
* Item between first middle and last **Optimal Choice: BigO = O(n log n)**
* Often 1st element (on left) is used **Bad Choice: Since we might end up with BigO = O(n^2), if the array is already sorted u will end up with O(n^2)**
* Often last (on right) item is used **Bad Choice: Since we might end up with BigO = O(n^2), if the array is already sorted u will end up with O(n^2)***

---
### **Example:** ###
Array: 17 41 5 22 54 6 29 3 13  
**Note: Left and right should traverse until all the values are been processed in a iteration**
* Pivot: Select Pivot = 22  
* Iteration Level #1:
  * 17 41 5 ***[22]*** 54 6 29 3 13   
    ```
    Left:   
    17 > 22 = No   
    41 > 22 = Yes (select left item to move)   
    Right:    
    13 < 22 = Yes   
    Swap:
    41 with 13   
    ```
  * 17 **41** 5 ***[22]*** 54 6 29 3 **13**
  * 17 **13** 5 ***[22]*** 54 6 29 3 **41**
* Rest of the Steps
  * 17 13 **5** ***[22]*** 54 6 29 **3** 41 **(Do Nothing Move Index)**
  * 17 13 5 ***[22]*** **54** 6 29 **3** 41 **(Swap Ready)**
  * 17 13 5 ***[22]*** **3** 6 29 **54** 41 **(Swap 1)**   
  * 17 13 5 **3** ***[22]*** 6 29 **54** 41 **(Swap 2)**   
  * 17 13 5 3 ***[22]*** **6** **29** 54 41   
  * 17 13 5 3 **6** ***[22]*** **29** 54 41   
  * 17 13 5 3 6 **22** 29 54   
* Iteration Level 2:   
  We have 2 partitions (exclude 22)   
  Partition 1: 17 13 5 3 6   
  Partition 2: 29 54   (this is already sorted)
  Partition 1 Processing
  * Pivot: 5 -> 17 13 ***5*** 3 6     
  * **17** 13 ***[5]*** 3 **6**   
  * **6** 13 ***[5]*** 3 **17**   
  * 6 **13** ***[5]*** **3** 17
  * 6 **3** ***[5]*** **13** 17
    * Sub 2 Partitions (Pivot: 5)
      * Left: 6 3
        * Pivot 3:
          * **6** ***[3]***
          * ***[3]*** **6**
      * Right: 13 17 (Sorted Nothing to do)
  * Output: **3 6 5 13 17**
* Final Output: 3 6 5 13 17 ***[22]*** 29 54
