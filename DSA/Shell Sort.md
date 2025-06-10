Shell sort, a variation of the insertion sort algorithm,was developed by David J. R. Anderson, a computer scientist and professor at the University of California, Berkeley as a way to sort large datasets in a relatively simple way.

The shell sort algorithm is as follows:
1. **Dividing the array**: Divide the input array into two subarrays, `a` and `b`, such that `a` is the left subarray and `b` is the right subarray.
2. **Comparing elements**: Compare each element in `a` with each element in `b`. If the element in `a` is smaller than the element in `b`, swap them.
3. **Repeating the process**: Repeat steps 1-2 until the entire array has been divided into subarrays.
4. **Building the sorted array**: Once the subarrays are sorted, combine them to form the final sorted array.

Here's its implementation in C++
```cpp
void shellSort(int arr[], int n) {
    //divide the array into two
    int gap = n / 2;
    while (gap > 0) {
        for (int i = gap; i < n; i++) {
            int temp = arr[i];
            int j = i;
            while (j >= gap && arr[j - gap] > temp) {
                arr[j] = arr[j - gap];
                j -= gap;
            }
            arr[j] = temp;
        }
        gap /= 2;
    }
}
```
