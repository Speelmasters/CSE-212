# Queues

Programs make use of many different times of data structures. A queue is a linear data structure that uses the First-In-First-Out(FIFO) rule. This means that items that are added to the data structure are also removed first. 

There are several ways to impliment a queue into a Python class. You can use a list ` variable = list()` , a Queue from the queue library can be initialized using `variable = Queue()`, and a deque from the collections library using `variable = deque()`.

When using either of the las two options, they must be imported using
```Python
from collections import deque
from queue import Queue
```

## Queue Methods

### Enqueue
Enqueue adds an item to the end of the queue. This method has essesntially the same for withever data structure you use for your queue. For a list and deque, you can use ` append()`  and for a Queue it is `put()`.
### Dequeue
Dequeue removes the item that was added least recently from the list or queue and returns the value that was stored  in that place. This is essentially helping or getting the the next "person" in line, or the next item to be removed from the queue. To dequeue a list, use `pop(0)`, in a Queue us `pop()` without the 0, and for deque use `get()`

## Example: Haircut Queue
In the example below, we will write a program that allows the user to add people to the queue and remove them. Before we write the code, we should amke a list of requirements that we want our code to handle.  Writing a list of requirements is an important step in writing software. In this example, we will be using the deque data structure.

Haircut Queue Requirements:
 - Allow user to add client
 - Allow user to get next client
 - Allow user to remove person if in the queue
 - Display all clients in queue


```Python
from collections import deque

clients = deque()
choice = ""
while(choice != "4"):
   print("Welcome to MEGA CUTS!")
   print("Please select and option")
   print("1) Add client")
   print("2) Remove client")
   print("3) Display next client")
   print("4) End program")

   choice = input()

   if (choice == "1"):
      new_client = input("Please enter clients name: ")
      clients.append(new_client)
   elif (choice == "2"):
      remove_client = input("Please enter clients name to be removed: ")
      if clients.__contains__(remove_client):
         clients.remove(remove_client)
         print(remove_client + " was removed from the queue")
      else:
         print(remove_client + " was not in the queue")
   elif (choice == "3"):
      print("Next client is " + clients.pop())
   elif (choice == "4"):
      pass
   else:
      print("Invalid Menu Selection")
```


## Problem to Solve: Limited Queue

Write a program that will only allow a certain number of items into a queue at a time. 

You can check your code with the solution here: [Solution](limited_queue.py)
