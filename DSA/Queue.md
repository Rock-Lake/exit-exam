A queue is an ordered [[List|list]] that follows the **First-In-First-Out**(FIFO)  interaction, this is done by having two operations:
- **Enqueue** – Inserts an item/element at the rear end of the queue. An overflow error occurs if the queue is full.
- **Dequeue** – Removes an item/element from the front end of the queue, and returns it to the user. An underflow error occurs if the queue is empty.

Queues can be implemented using [[Array|arrays]] or [[Linked List|linked lists]] their performance is as follows:

| Operations | Array implementation | Linked list implementation |
| ---------- | -------------------- | -------------------------- |
| Enqueue    | O(1)                 |                            |
| Dequeue    | O(1)                 |                            |
