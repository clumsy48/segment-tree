# Why use ?

## To perform range queries
```
Example : A[] = {1,4,2,6,9}
          sum in range 2-4
```
## Before segment tree

###       Method 1 : Naiive     
```
          retrieval : O(n)  iterate from L to R
          update    : O(1)  update at index x
          Not good if retireval is comparitively larger than update
```
###       Method 2 : Prefix Sum 

          A[] = {1,4,2,6,9} 
          S[] = {1,5,7,13,22}
          retrieval : O(1)  S[R]-S[L-1]
          update    : O(n)  update at index x in A will require update from x to n-1 in S
          Not good if update is comparitively larger than retrieve

###       Method 3 : Segment Tree
          retrieval : O(log n)  
          update    : O(log n)
          
1. Size of Segment Tree

  ![Alt Text](https://github.com/clumsy48/segment-tree/blob/theory/segment_tree.jpg)
```
total size = 2^0 + 2^1 + 2^2 + .... + 2^ceil( logn(n) )  
           = ( 1 * ( 2^ (ceil( logn(n) ) + 1) - 1) ) / (2 -1)
           = 2 * 2^ (ceil( logn(n) )) 
           ~ 4n
 
```
          

          
                    



