An array is continuous yet fixed range of memory that stores values of single datatype. This fixed range is the size of the array assigned during declaration. 
```C++
dataType arrayName[size] = {"element", "element",...};
```

Each Element in an array contains a positional value called "index" that starts from the 0th position in the array.

Due to the continuous memory, [[Data Structures and Algorithms#^70d2a5|reading]] an element from an array is easy; however [[Data Structures and Algorithms#^e63471|searching]] a value is computationally expensive since it has to check each element against the search value. Additionally, [[Data Structures and Algorithms#^8c0303|inserting]] or [[Data Structures and Algorithms#^2d8491|deleting]] a value can be slow depending on the index it will be add or delete the value. Since it may have to shift every next element to the side so the value will be added or deleted.

