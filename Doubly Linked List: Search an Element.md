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
