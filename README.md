# 📚 Doubly Linked List: Insert Elements at the End of a Doubly Linked List

This Python program demonstrates the creation and manipulation of a **Doubly Linked List** where elements can be inserted at the **end** of the list. The program also provides a method to traverse the list and display the elements.
---
## 🎯 Aim

To write a Python program that:
- Implements a **Doubly Linked List**.
- Allows insertion of elements at the end of the list.
- Provides functionality to traverse the list and display its elements.
---
## 🧠 Algorithm
1. **Step 1:** Define a class `Node` to represent each node in the doubly linked list with attributes:
   - `item` for storing the data of the node.
   - `nref` for storing the reference to the next node.
   - `pref` for storing the reference to the previous node.
2. **Step 2:** Define a class `DoublyLinkedList` with:
   - `start_node` to point to the first node of the list.
3. **Step 3:** Define methods in the `DoublyLinkedList` class:
   - `insert_in_emptylist(data)` to insert an element when the list is empty.
   - `insert_at_end(data)` to insert elements at the end of the list.
   - `traverse_list()` to traverse the list and print the elements.
4. **Step 4:** Create an instance of `DoublyLinkedList` and use the `insert_at_end()` method to insert elements into the list.
5. **Step 5:** Use the `traverse_list()` method to print the elements of the list.
---
## 💻 Program
 class Node:
 def init (self, data): 
 self.item = data 
  self.nref = None 
self.pref = None
class DoublyLinkedList: 
def init (self):
 self.start_node = None
 def insert_in_emptylist(self, data): 
if self.start_node is None:
   new_node = Node(data) 
 self.start_node = new_node
else:          
   print("list is not empty") 
def insert_at_end(self,data):
 new_node = Node(data) 
ifself.start_node is None:.
self.start_node = new_node 
else:
 print("list is not empty")
 def insert_at_end(self, data):
new_node = Node(data) 
 ifself.start_node is None:
self.start_node = new_node 
else:
n = self.start_node
 while n.nref is not None:
   n = n.nref
 n.nref = new_node 
 new_node.pref = n
  def traverse_list(self)
 if self.start_node is None:
   print("List has no element") 
 return
else:
  n = self.start_node 
   while n is not None:
 print(n.item , " ") 
 n = n.nref
  new_linked_list = DoublyLinkedList() 
new_linked_list.insert_at_end(10) 
 new_linked_list.insert_at_end(20)
new_linked_list.insert_at_end(30) 
 new_linked_list.insert_at_end(40) 
 new_linked_list.traverse_list()
## Sample Output
<img width="390" height="150" alt="image" src="https://github.com/user-attachments/assets/7008f7e0-f695-4b74-adf7-d6536358ed3e" />


## Result
Thus the program has been successfully executed

# 📝 Doubly Linked List: Search an Element

This Python program demonstrates the implementation of a **Doubly Linked List** where you can insert elements at both the beginning and the end of the list. Additionally, it allows you to search for a specific element in the list.

---

## 🎯 Aim

To write a Python program that:
- Implements a **Doubly Linked List** with functions to insert elements at the beginning and the end of the list.
- Implements a search function to check if a given element exists in the list.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Nodeq` with:
   - `data` to store the node's value.
   - `next` to store the reference to the next node.
   - `prev` to store the reference to the previous node.

2. **Step 2:** Define a class `DoublyLinkedList` with:
   - `head` to point to the first node.

3. **Step 3:** In the `DoublyLinkedList` class, define methods:
   - `insert_beginning(data)` to insert a node at the beginning.
   - `insert_end(data)` to insert a node at the end.
   - `search(data)` to search for an element in the list.

4. **Step 4:** Create an instance of `DoublyLinkedList`.
   - Insert elements at the beginning and end.
   - Search for specific elements.

---

## 💻 Program
class Node q: <br>
def init (self, data):  <br>
   self.data = data  <br>
   self.next = None  <br>
   self.prev = None  <br>
class DoublyLinkedList:  <br>
   def init (self):  <br>
      self.head = None   <br>
   def insert_beginning(self,data):  <br>
      new_node = Nodeq(data)  <br>
      if(self.head == None):  <br>
         self.head = new_node  <br>
         return  <br>
      self.head.prev = new_node  <br>
      new_node.next = self.head  <br>
      self.head = new_node  <br>

def insert_end(self, new_data):  <br>
      new_node = Nodeq(new_data)   <br>
      if self.head is None:  <br>
         new_node.prev = None   <br>
         self.head = new_node  <br>
         return  <br>
      last = self.head  <br>
while last.next:  <br>
      last = last.next  <br>
      last.next = new_node  <br>
      new_node.prev = last  <br>
def search(self,data):  <br>
      current = self.head  <br>
while current:  <br>
      if current.data == data:  <br>
         return True  <br>
      current = current.next  <br>
print("The given data doesnot exist:")  <br>
      return False  <br>
Dllist = DoublyLinkedList()  <br>
Dllist.insert_beginning(2)  <br>
Dllist.insert_end(0)  <br>
Dllist.insert_end(1)  <br>
print(Dllist.search(0))  <br>
print(Dllist.search(3))

## Sample Output
<img width="461" height="143" alt="image" src="https://github.com/user-attachments/assets/9295f0be-0d84-49ad-8aff-cfbdd035cb6e" />

## Result
Thus the program has been successfully executed
# 📚 Singly Linked List : Find the Middle Node of a Singly Linked List Using Recursion

This Python program demonstrates how to find the middle node of a singly linked list using recursion. The program calculates the middle element by utilizing two pointers, with one pointer moving one step at a time (slow) and the other moving two steps at a time (fast). When the fast pointer reaches the end of the list, the slow pointer will be at the middle node.

## 🎯 Aim

To write a Python program that:
- Creates a singly linked list.
- Uses recursion to find the middle node of the list.
- In case of an even number of nodes, it returns the second middle element.

## 🧠 Algorithm

1. **Node Class**: 
   - Define a `Node` class to represent each node in the singly linked list. Each node has two attributes: `data` and `next`.
   
2. **LinkedList Class**:
   - Define a `LinkedList` class that manages the linked list with methods to:
     - `append(data)`: Add a new node to the end of the list.
     - `get_middle_recursive(slow, fast)`: A recursive helper function to find the middle node using two pointers (slow and fast).
     - `find_middle()`: A method to call the recursive function and return the middle node's data.

3. **Input**:
   - First, the program reads an integer `n`, representing the number of elements in the linked list.
   - Then, it reads `n` space-separated integers to form the linked list.

4. **Recursive Middle Finding**:
   - The `get_middle_recursive` method uses two pointers to traverse the list:
     - The `slow` pointer moves one step at a time.
     - The `fast` pointer moves two steps at a time.
   - When the `fast` pointer reaches the end, the `slow` pointer will be at the middle node.

5. **Output**:
   - The program prints the middle element. If the list has an even number of nodes, it returns the second middle element.

---

## 💻 Program
class Node:  <br>
    def __init__(self, data): <br>
       self.data = data <br>
       self.next = None<br>
class LinkedList:<br>
 
  def __init__(self):<br>
       self.head = None<br>
    def append(self, data):<br>
       new_node = Node(data)<br>
       if not self.head:<br>
          self.head = new_node<br>
          return<br>
       temp = self.head<br>

   while temp.next:<br>
          temp = temp.next<br>
          temp.next = new_node<br>
    def get_middle_recursive(self, slow, fast):<br>
      if not fast or not fast.next:<br>
          return slow # Return the middle node<br>
          return self.get_middle_recursive(slow.next, fast.next.next)<br>
    def find_middle(self):<br>
       if not self.head:<br>
          return None<br>
       middle_node = self.get_middle_recursive(self.head, self.head)<br>
          return middle_node.data if middle_node else None<br>
         n = int(input().strip()) # Number of elements<br>
         arr = list(map(int, input().strip().split())) # Linked list elements<br>
# Create linked list and append elements<br>
ll = LinkedList()<br>
for num in arr:<br>
    ll.append(num)<br>
# Find and print middle element<br>
print(ll.find_middle())

## Sample Input & Output
<img width="329" height="144" alt="image" src="https://github.com/user-attachments/assets/0bd935f0-3289-46f2-aec5-f37eb3072b52" />

## Result


Thus, the Python program has been created and executed successfully ..
# # 🔍 Singly Linked List-To Search an Element in a Linked List

This project contains a simple implementation of a **singly linked list** in Python, allowing insertion and searching of elements.

---

## 🎯 Aim

To write a Python program to search for a given element in a singly linked list using object-oriented programming principles.

---

## 🧠 Algorithm

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

---

## 💻 Program
class Node:<br>
   def init (self, data):<br>
      self.data = data <br>
      self.next = None<br>
class LinkedList:<br>
   def init (self):<br>
      self.head = None<br>
   def push(self, new_data): <br>
      new_node = Node(new_data) <br>
      new_node.next = self.head <br>
      self.head = new_node<br>
   def search(self, x): <br>
      current = self.head <br>
      while current:<br>
         if current.data == x: <br>
            return True<br>
      current = current.next <br>
         return False<br>
llist = LinkedList() <br>
llist.push(10); <br>
llist.push(30); <br>
llist.push(11); <br>
llist.push(21);<br>
llist.push(14);<br>
   data = int(input()) <br>
   if llist.search(data):<br>
      print("Yes") <br>
   else:<br>
      print("No")
## Sample Output
<img width="224" height="120" alt="image" src="https://github.com/user-attachments/assets/2adb245b-48f5-4eac-8344-0c3dc4cce979" />

## Result

Thus the program has been successfully executed
# 📝 Singly Linked List: Add Element at the Start

This Python program demonstrates the implementation of a **Singly Linked List** where a new element can be added at the **start** of the list.

---

## 🎯 Aim

To write a Python program that adds a **new element** at the **start** of a singly linked list. The program implements a `push_front` method that inserts an element at the front of the list, followed by a method to print the list.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Node` with:
   - `data` to store the node's value.
   - `next` to store the reference to the next node.
   
2. **Step 2:** Define a class `LinkedList` with:
   - `head` to point to the first node.
   
3. **Step 3:** In the `LinkedList` class, define a method `push_front(newElement)`:
   - Create a new node with `newElement`.
   - Set the new node's next pointer to the current head node.
   - Set the head to the new node.

4. **Step 4:** Define a method `PrintList()` to display the list:
   - Print the elements of the list or display "The list is empty." if the list is empty.

5. **Step 5:** Instantiate a `LinkedList` object, `MyList`, and add elements at the start using the `push_front()` method.

6. **Step 6:** Call the `PrintList()` method to display the list.

---

## Program
class Node:<br>
   def init (self, data): <br>
      self.data = data <br>
      self.next = None<br>
class LinkedList:<br>
   def init (self):<br>
      self.head = None<br>
   def push(self, new_data): <br>
      new_node = Node(new_data) <br>
      new_node.next = self.head <br>
      self.head = new_node<br>
   def search(self, x): <br>
      current = self.head <br>
      while current:<br>
         if current.data == x: <br>
            return True<br>
      current = current.next <br>
         return False<br>
llist = LinkedList() <br>
llist.push(10); <br>
llist.push(30);<br> 
llist.push(11); <br>
llist.push(21);<br>
llist.push(14);<br>
   data = int(input()) <br>
   if llist.search(data):<br>
      print("Yes") <br>
   else:<br>
      print("No")
## Sample Output
<img width="224" height="120" alt="image" src="https://github.com/user-attachments/assets/519150ee-9aa0-4035-80cb-5910116aab04" />

## Result
Thus the program has been successfully executed
