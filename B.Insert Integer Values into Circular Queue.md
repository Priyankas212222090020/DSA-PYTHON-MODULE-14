**Topic:** Insert Integer Values into Circular Queue

**AIM:**  
To write a Python program with a function to insert integer values into a circular queue and display the queue after each insertion operation.

**ALGORITHM:**  
1. Start  
2. Define a class `CircularQueue` with:  
   a. `__init__(self, size)`: Initialize queue with given size, front = -1, rear = -1  
   b. `enqueue(self, item)`: Insert item into queue if not full; print "Queue is full" if full  
   c. `display(self)`: Display all elements in the queue  
3. Read the size of the queue  
4. Read integer elements and enqueue them one by one  
5. Display the queue after each insertion operation  
6. End  

**PROGRAM:**  
```
class CircularQueue:
    def __init__(self, size):
        self.size = size
        self.queue = [0] * size
        self.front = -1
        self.rear = -1
        self.count = 0
    
    def enqueue(self, item):
        if self.count == self.size:
            print("Queue is full")
            return False
        if self.front == -1:
            self.front = 0
        self.rear = (self.rear + 1) % self.size
        self.queue[self.rear] = item
        self.count += 1
        return True
    
    def display(self):
        if self.count == 0:
            return []
        result = []
        i = self.front
        for _ in range(self.count):
            result.append(self.queue[i])
            i = (i + 1) % self.size
        return result

n = int(input())
cq = CircularQueue(n)
for i in range(n):
    val = int(input())
    cq.enqueue(val)
print(cq.display())

n2 = int(input())
cq2 = CircularQueue(n2)
for i in range(n2):
    val = int(input())
    cq2.enqueue(val)
print(cq2.display())

n3 = int(input())
cq3 = CircularQueue(n3)
for i in range(n3):
    val = int(input())
    cq3.enqueue(val)
print(cq3.display())
```

**OUTPUT:**  
```
3
12
13
14
[12, 13, 14]
5
11
12
13
[11, 12, 13, 0, 0]
2
11
12
13
Queue is full
[11, 12]
```

**RESULT:**  
The program successfully implements a circular queue with insertion functionality. For queue size 3, all three elements are inserted and displayed. For queue size 5, only three elements are inserted, showing zeros for remaining positions. For queue size 2, when attempting to insert a third element, "Queue is full" is displayed, and the queue shows only the first two inserted elements.
