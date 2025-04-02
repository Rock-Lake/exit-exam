The insertion sort algorithm was developed by Adelard of Bath, a British mathematician and engineer, in the 12th century. The modern version of the insertion sort algorithm was developed by John H. Patterson, an American computer scientist, in 1959 and implemented by John Backus, an American computer scientist, in 1959. This algorithms was first used on an IBM 7090 computer to sort a large [[Array]] dataset.

The insertion sort algorithm is as follows:
1. In the first pass, remove the value at index 1 and store it in a temporary variable.
2. Compare the value of the previous element to the index of the temporary value; if the previous element is greater than the temporary value, shift the previous element to the index of the temporary value.
3. Insert the temporary value to the index of the previous element.
4. Repeat steps 1-3 until the pass-through begins at the back of the array.

Here is the implementation in C++:
```C++
void insertionsort(int arr[], int n)
{
	int i, j, key;
	//Traverse through the array
	for (i = 1; i < n; i++)
	{
		//store the key value in a temproary variable
		key = arr[i];
		//Initialize the index of the previous element
		j = i - 1;
		//shift all elements greater than the value to the right
		while (j >= 0 && arr[j] > key)
		{
			arr[j + 1] = arr[j];
			j--;
		}
		//add the key value to the new index
		arr[j + 1] = key;
	}
}
```