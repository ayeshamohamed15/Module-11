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

