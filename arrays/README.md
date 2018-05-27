# Arrays

* Contiguous memory allocation and constraint of equal size elements makes accessing array elements simple arithmetic and constant time effort.
    * ```array_address + element_size * (index_desired - index_initial) ```. ```initial_index``` is generally 0.
* Multi-dimensional arrays, although pictorial representation is multi-dimensional but still arrays need to be stored in contiguous memory locations. Therefore multi-dimensional arrays are stored as **row major** or **column major** scheme. 
    * **Row major** wherein column index changes frequently.

        ```(1,1),(1,2),(1,3),(2,1),(2,2),(2,3)```
    * While in **column major** row index changes frequently.

        ```(1,1),(2,1),(3,1),(1,2),(2,2),(3,2)```

## Time Complexity

### Read/Update 
* O(1)

### Add/Remove
* At the end - O(1)
    * We know size of the array, hence finding the element where we need to write is constant time.
* At the beginning - O(n)
    * Before insert, we will have to shift all n elements to right.
    * After delete, we will have to shift all n elements to left.
* In-between - O(n)
    * Similar to write at the beginning, some elements will go left and some right.
* Even during write, having constant access time is advantage.
    
