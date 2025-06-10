A linked list is a dynamic data structure that links entities which consists of two parts:
- **Data Node** - holds a struct of one or more variables
- **Pointer** - holds the address to the adjacent node
The number of pointer in a linked list can classify into two types of linked lists:
- **Single linked list**
```C++
struct ListName{
	dataType Data_Node;
	struct ListName *next;
}
//during initializaion, the linked list is empty
struct ListName *start = NULL;
```

- **Double linked list**
```C++
struct ListName{
	struct ListName *previous;
	dataType Data_Node;
	struct ListName *next;
}
//during initializaion, the linked list is empty
struct ListName *start = NULL;
```
