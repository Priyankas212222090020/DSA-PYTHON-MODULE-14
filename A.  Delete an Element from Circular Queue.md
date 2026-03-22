**Topic:** Delete an Element from Circular Queue

**AIM:**  
To write a Python function to delete a string element from a circular queue by removing the front element.

**ALGORITHM:**  
1. Start  
2. Define a class `CircularQueue` with:  
   a. `__init__(self, size)`: Initialize queue with given size, front = -1, rear = -1  
   b. `enqueue(self, item)`: Add item to queue if not full  
   c. `dequeue(self)`: Remove and return front element if queue not empty  
   d. `display(self)`: Display all elements in the queue  
3. Read the size of the queue  
4. Read the elements and enqueue them  
5. Display the queue before deletion  
6. Perform dequeue operation to delete the front element  
7. Display the queue after deletion  
8. End  

**PROGRAM:**  
```
class CircularQueue:
    def __init__(self, size):
        self.size = size
        self.queue = [None] * size
        self.front = -1
        self.rear = -1
    
    def enqueue(self, item):
        if (self.rear + 1) % self.size == self.front:
            return
        if self.front == -1:
            self.front = 0
        self.rear = (self.rear + 1) % self.size
        self.queue[self.rear] = item
    
    def dequeue(self):
        if self.front == -1:
            return None
        item = self.queue[self.front]
        if self.front == self.rear:
            self.front = -1
            self.rear = -1
        else:
            self.front = (self.front + 1) % self.size
        return item
    
    def display(self):
        if self.front == -1:
            return []
        result = []
        i = self.front
        while True:
            result.append(self.queue[i])
            if i == self.rear:
                break
            i = (i + 1) % self.size
        return result

n = int(input())
cq = CircularQueue(n)
for i in range(n):
    cq.enqueue(input())
print(cq.display())
cq.dequeue()
print(cq.display())
```

**OUTPUT:**  
```
3
java
python
c++
['java', 'python', 'c++']
['python', 'c++']
```
<img width="1375" height="447" alt="image" src="https://github.com/user-attachments/assets/66d690ef-716e-40e1-8292-bf638e7b04e4" />

**RESULT:**  
The program successfully implements a circular queue and deletes a string element from the front. For input size 3 with elements "java", "python", "c++", the queue before deletion shows all three elements, and after deletion shows the remaining two elements "python" and "c++".
