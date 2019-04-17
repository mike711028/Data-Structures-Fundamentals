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
 
    1. row 1 and 2 which we don't use
 
 ```(3 - 1) * 6 ```
