**Topic:** Insert Elements at Front End of Deque Using Collections Module

**AIM:**  
To write a Python program to insert integers 14 and 15 at the front end of a deque using the built-in collections module.

**ALGORITHM:**  
1. Start  
2. Import the deque class from collections module  
3. Create an empty deque  
4. Read three integers from the user and append them to the deque using `append()` method  
5. Insert integers 14 and 15 at the front end of the deque using `appendleft()` method  
6. Display the deque with the message "The deque after appending is :"  
7. End  

**PROGRAM:**  
```
from collections import deque

d = deque()
for i in range(3):
    d.append(int(input()))
d.appendleft(15)
d.appendleft(14)
print("The deque after appending is :")
print(d)
```

**OUTPUT:**  
```
11
12
13
The deque after appending is :
deque([15, 14, 11, 12, 13])
```

**RESULT:**  
The program successfully uses the collections module to create a deque and inserts elements at the front end using the `appendleft()` method. For input integers 11, 12, 13, the deque initially contains these three elements, and after inserting 15 and 14 at the front, the final deque shows all five elements with 15 and 14 at the beginning in the order they were inserted.
