# Lecture: Arrays
Definition: 

Array: **Contiguous area of the memory consisting of equal-size elements indexed by contiguous integers**

|1 |2 |3 |4 |5 |6 |
|-|-|-|-|-|-|

   + zero-based indexing starts from 0
   + one-based indexing starts from 1

## What's special about array?
   + we have constant-time access to any particular element in an array
   + constant-time access to read and write
   
How much time does we want to access the certain address we're intereste in?

we start with the address of the array

``` array_address + elem_size * (i - first_index)  // start from 1 instead of 0```
## Multi-Dimensions Array

 |(1,1) |(1,2) |(1,3) |(1,4) |(1,5) |(1,6)|
 |:---:|:---:|:---:|:---:|:---:|:---:|
 | (2,1)|(2,2) |(2,3) |(2,4) | (2,5)|(2,6) |
 |(3,1) |(3,2) |(3,3) | * (3.4)|(3,5) |(3,6) |
 
How do you find the address of the element (3,4) ?
 
1. calculate empty elements in row 1 and 2
```
(3 - 1) * 6
```
2. calculate the rest of empty elements before (3,4) // from left to right
```
(4 - 1)
```
3. sum them up
```
(3 - 1) * 6 + (4 - 1) = 15
```
4. multiply 15 by element size
```
elem_size * ((3 - 1) * 6 + (4 - 1))
```
5. finally, after adding array address, we get the address of our element (3,4)
```
array_addr + elem_size * ((3 - 1) * 6 + (4 - 1))
```

## Row-major and Column-major

   + Multi-dimensions array
 
|(1,1) |(1,2) |(1,3) |(1,4) |(1,5) |(1,6)|
|:---:|:---:|:---:|:---:|:---:|:---:|
| (2,1)|(2,2) |(2,3) |(2,4) | (2,5)|(2,6) |
|(3,1) |(3,2) |(3,3) | * (3.4)|(3,5) |(3,6) |

   + Row-major indexing or Row-major ordering
   
the column index is changing rapidly

|(1,1) |
|:---:|
|(1,2) |
|(1,3) |
|(1,4) |
|(1,5) |
|(1,6)|
| (2,1)|
|..... |

   + Column-major indexing or Column-major ordering

the row index is changing rapidly
 
|(1,1) |
|:---:|
|(2,1) |
|(3,1) |
|(1,2) |
|(2,2) |
|(3,2)|
|(1,3)|
|..... |

## Times for Common Operations
