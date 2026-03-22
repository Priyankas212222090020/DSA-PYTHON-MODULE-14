**Topic:** Insert Elements at Rear End of Deque Using Collections Module

**AIM:**  
To write a Python program to insert characters 'h', 'o', 'n' at the rear end of a deque using the built-in collections module.

**ALGORITHM:**  
1. Start  
2. Import the deque class from collections module  
3. Create an empty deque  
4. Read three characters from the user and append them to the deque using `append()` method  
5. Append the characters 'h', 'o', 'n' to the deque using `append()` method  
6. Display the deque with the message "The deque after appending at right is :"  
7. End  

**PROGRAM:**  
```
from collections import deque

d = deque()
for i in range(3):
    d.append(input())
d.append('h')
d.append('o')
d.append('n')
print("The deque after appending at right is :")
print(d)
```

**OUTPUT:**  
```
p
y
t
The deque after appending at right is :
deque(['p', 'y', 't', 'h', 'o', 'n'])
```

**RESULT:**  
The program successfully uses the collections module to create a deque and inserts elements at the rear end using the `append()` method. For input characters 'p', 'y', 't', the deque initially contains these three elements, and after appending 'h', 'o', 'n', the final deque shows all six elements in order.
