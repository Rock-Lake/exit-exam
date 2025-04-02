Developed by Russian mathematicians and computer scientists Adelson-Velskii and Landis in 1959, It is one of the earliest [[Array|array]] sorting algorithm in history.

The bubble sort algorithm follows these steps:
1. Point to two consecutive values in the array, this is usually arr\[0] and arr\[1].
2. If the second value is larger than the first swap the position of the two elements.
3. Shift the pointers one cell to the right.
4. Repeat steps 1-3 until we reach the end of the array
5. move the 2 pointers back to the first 2 indexes of the array and repeat steps 1-4 until the array is sorted.

Its implementation in C++ is as follows:
```C++
void bubblesort(int arr[], int n)
{
    int i, j, temp;
    // Traverse through all array elements
    for (i = 0; i < n - 1; i++) 
    {
        // Last i elements are already in place
        for (j = 0; j < n - i - 1; j++) 
        {   // Traverse the array from 0 to n-i-1
            // Swap if the element found is greater than the next element
            if (arr[j] > arr[j + 1]) 
            {
               temp = arr[j]
               arr[j] = arr[j+1];
               arr[j+1] = temp
            }
        }
    }
}

```

This algorithm has an asymptotic runtime of $\Theta(N^2)$ since it has a nested for loop to sort the array.