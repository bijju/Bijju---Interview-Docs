# **Merge Sort **
merge sort (also commonly spelled mergesort) is an efficient, general-purpose, comparison-based sorting algorithm. Most implementations produce a stable sort, which means that the implementation preserves the input order of equal elements in the sorted output. Merge sort is a divide and conquer algorithm that was invented by John von Neumann in 1945.[2] A detailed description and analysis of bottom-up mergesort appeared in a report by Goldstine and von Neumann as early as 1948.

## **Big O Analysis **
* O(n log n)
* Is Recursive method by implementing Divide and Conquer algorithm
* Very efficient against large datasets
* Merge sort does log n merge steps because each step double the list size, I does n work for each merge step because it must look at every item

## **Example**
**Example: 1**  
2 4 3 1  
Split  
[ **2** **4** ] <> [ **3** **1** ]   
[ **2** 4 ] <> [ **1** 3 ] => [1]   
[ **2** 4 ] <> [ **3** ] => [1 2]   
[ **4** ] <> [ **3** ] => [1 2 3 ]   
[ **4** ] <> [ ] => [1 2 3 4]  

**Example: 2**  
  * [17 87 6 22 41 3 13 54 ]
    * [17 87 6 22] <> [41 3 13 54]
    * [ [17 87] -- [6 22] ] <> [ [41 3] -- [13 54] ]
    * [ [ [**17**] ~  [**87**] ] -- [ [6] ~ [22] ] ] <> [ [ [41] ~ [3] ] -- [[13] ~ [54]] ] - Sort and merge
    * [ [17, 87] -- [ [**6**] ~ [**22**] ] ] <> [ [ [41] ~ [3] ] -- [[13] ~ [54]] ] - Sort and merge
    * [ [17, 87] -- [6, 22] ] <> [ [ [**41**] ~ [**3**] ] -- [[13] ~ [54]] ] - Sort and merge
    * [ [17, 87] -- [6, 22] ] <> [ [3, 41] -- [[**13**] ~ [**54**]] ] - Sort and merge
    * [ [**17**, 87] -- [**6**, 22] ] <> [ [**3**, 41] -- [**13**, 54] ] - Sort and merge
    * [ [6] << [**17**, 87] -- [**22**] ] <> [ [3] << [**41**] -- [**13**, 54] ] - Sort and merge
    * [ [6, 17] << [**87**] -- [**22**] ] <> [ [3, 13] << [**41**] -- [**54**] ] - Sort and merge
    * [**6**, 17, 22, 87] <> [**3**, 13, 41, 54] - Sort and merge
    * [3] << [**6**, 17, 22, 87] <> [**13**, 41, 54] - Sort and merge
    * [3, 6] << [**17**, 22, 87] <> [**13**, 41, 54] - Sort and merge
    * [3, 6, 13] << [**17**, 22, 87] <> [**41**, 54] - Sort and merge
    * [3, 6, 13, 17] << [**22**, 87] <> [**41**, 54] - Sort and merge
    * [3, 6, 13, 17, 22] << [**87**] <> [**41**, 54] - Sort and merge
    * [3, 6, 13, 17, 22, 41] << [**87**] <> [**54**] - Sort and merge
    * [3, 6, 13, 17, 22, 41, 54, 87] - **Done!**
