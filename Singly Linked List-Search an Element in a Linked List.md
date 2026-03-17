# # Singly Linked List-To Search an Element in a Linked List

This project contains a simple implementation of a **singly linked list** in Python, allowing insertion and searching of elements.



##  Aim

To write a Python program to search for a given element in a singly linked list using object-oriented programming principles.



## Algorithm

1. **Define a Node class** with `data` and `next` attributes.
2. **Define a LinkedList class** with:
   - A `head` pointer initialized to `None`.
   - A `push()` method to add elements at the beginning.
   - A `search()` method to check whether a given value exists.
3. Create a `LinkedList` instance.
4. Insert the elements **10, 30, 11, 21, 14** using `push()` (which results in reverse order).
5. Read an integer input from the user.
6. Use `search()` to check if the element exists in the list.
7. Output **"Yes"** if found, else **"No"**.



##  Program
```
class Nodeq: 
    def __init__(self, data): 
        self.data = data 
        self.next = None 
        self.prev = None 

class DoublyLinkedList: 
    def __init__(self): 
        self.head = None 

    def insert_beginning(self, data): 
        new_node = Nodeq(data) 
        if self.head is None: 
            self.head = new_node 
            return 
        self.head.prev = new_node 
        new_node.next = self.head 
        self.head = new_node 

    def insert_end(self, new_data): 
        new_node = Nodeq(new_data) 
        if self.head is None: 
            new_node.prev = None 
            self.head = new_node 
            return 
        last = self.head 
        while last.next: 
            last = last.next 
        last.next = new_node 
        new_node.prev = last 

    def search(self, data): 
        current = self.head 
        while current: 
            if current.data == data: 
                return True 
            current = current.next 
        print("The given data does not exist:") 
        return False 

# Main
Dllist = DoublyLinkedList() 
Dllist.insert_beginning(2) 
Dllist.insert_end(0) 
Dllist.insert_end(1) 

print(Dllist.search(0))  # Output: True
print(Dllist.search(3))  # Output: The given data does not exist: \n False

```
## Output
   ![image](https://github.com/user-attachments/assets/33f82914-9191-41eb-999c-984041dce3c4)

## Result
Thus the program has been successfully executed.

