Developed by Russian mathematicians and computer scientists Adelson-Velskii and Landis in 1960, the selection sort is an [[Array]] sorting algorithm designed to surpass the limitations of [[Bubble Sort]].

The selection sort algorithm is as follows:
1. Check each cell of the array from left to right to find and track the lowest value.
2. Swap the position of the lowest value with the first element of the unsorted part of the array.
3. Repeat steps 1&2 until the the first element of the unsorted array becomes the back of the array.

Its implementation in C++ is as follows:
```C++
void selectionsort(int arr[], int n)
{
	int i,j,temp,low;
	for(i = 0; i < n; i++)
	{
		low = i;//Takes the index of the first element of the unsolved array
		for(j = i; j < n; j++)
		{
			if (arr[low] > arr[j])//checks if low's element is larger
			{
				low = j;//updates lowest value index
			}
		}
		if(low != i)
		//checks if low's index isn't i, if so it swaps elements
		{
			temp = arr[low];
			arr[low ]= arr[i];
			arr[i] = temp;
		}
}
```

This is the improvement of selection sort compared to bubble sort

| N Elements | Max no. of steps in bubble sort | Max no. of steps in selection sort |
| ---------- | ------------------------------- | ---------------------------------- |
| 5          | 20                              | 14                                 |
| 10         | 90                              | 54                                 |
| 20         | 380                             | 199                                |
| 40         | 1560                            | 819                                |
| 80         | 6320                            | 3239                               |
