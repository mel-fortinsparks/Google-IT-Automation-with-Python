## While Loops
#### What is a while loop?
```
x = 0
while x < 5:
  print("Not there yet, x=" + str(x))
  x = x + 1
print("x=" + str(x))
```
Question: How many times will "Not there yet" be printed?<br>
Answer: 5

#### Question
Can you work out what this function does? Try passing different parameters to the attempts function to see what it does. 
```
def attempts(n):
    x = 1
    while x <= n:
        print("Attempt " + str(x))
        x += 1
    print("Done")
    
attempts(5)
```
Answer: We initialize the function with x equal to 1, and then we enter our *while* loop,
which checks to see if value of the x-variable is less than the parameter n that the function recieved.
If that comparison evaluates to True, then the code inside the *while* block is executed. When the n-variable is entered as 5, the loop will continue to print() until x becomes larger than 5 (which would be 6 in this case). When the x-variable becomes equal to 6, the loop finishes and the function prints "Done".

#### Question
In this code, there's an initialization problem that's causing our function to behave incorrectly. Can you find the problem and fix it?
<br>**Before:**
```
def count_down(start_number):
  while (current > 0):
    print(current)
    current -= 1
  print("Zero!")

count_down(3)
```
**After:**
```
def count_down(start_number):
  current=start_number
  while (current > 0):
    print(current)
    current -= 1
  print("Zero!")

count_down(3)
```
