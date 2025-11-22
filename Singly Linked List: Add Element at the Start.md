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
