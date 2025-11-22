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
