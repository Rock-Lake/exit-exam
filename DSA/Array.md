An array is continuous yet fixed range of memory addresses that stores values of single datatype. This fixed range is the size of the array assigned during declaration. 
```C++
dataType arrayName[size] = {"element", "element",...};
```

Each Element in an array contains a positional value called "index" that starts from the 0th position in the array.

Due to the continuous memory, [[Data Structures and Algorithms#^70d2a5|reading]] or [[Data Structures and Algorithms#^d879d9|updating]] an element from an array is easy; however [[Data Structures and Algorithms#^e63471|searching]], [[Data Structures and Algorithms#^8c0303|inserting]] or [[Data Structures and Algorithms#^2d8491|deleting]] a value can be slow depending on the index it will be add or delete the value. More specifically:

| Location                   | Searching   | Inserting   | Deleting    |
| -------------------------- | ----------- | ----------- | ----------- |
| First location, arr\[0]    | $\Theta(1)$ | $\Theta(N)$ | $\Theta(N)$ |
| $k^{th}$ location, arr\[k] | $\Theta(N)$ | $\Theta(N)$ | $\Theta(N)$ |
| Last location, arr\[n]     | $\Theta(N)$ | $\Theta(1)$ | $\Theta(1)$ |

