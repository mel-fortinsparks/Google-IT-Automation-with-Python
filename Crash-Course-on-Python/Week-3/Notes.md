## While Loops
### What is a while loop?
#### Question: 
How many times will "Not there yet" be printed?
```
x = 0
while x < 5:
  print("Not there yet, x=" + str(x))
  x = x + 1
print("x=" + str(x))
```
Answer: 5

### More while loop examples
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

### Why initializing variables matters
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
### Infinite loops and how to break them
#### Question
The following code causes an infinite loop. Can you figure out what’s missing and how to fix it?
<br>**Before:**
```
def print_range(start, end):
	# Loop through the numbers from start to end
	n = start
	while n <= end:
		print(n)
```
**After:**
```
def print_range(start, end):
	# Loop through the numbers from start to end
	n = start
	while n <= end:
		print(n)
		n+=1
```
## For Loops
### What is a for loop?
#### Question
Fill in the gaps of the sum_squares function, so that it returns the sum of all the squares of numbers between 0 and x (not included). Remember that you can use the range(x) function to generate a sequence of numbers from 0 to x (not included).<br>
**Before**
```
def square(n):
    return n*n

def sum_squares(x):
    sum = 0
    for n in ___:
        sum += __
    return __

print(sum_squares(10)) # Should be 285
```
**After:**
```
def square(n):
    return n*n

def sum_squares(x):
    sum = 0
    for n in range(x):
        sum += square(n)
    return sum

print(sum_squares(10)) # Should be 285
```
### More for loop examples
#### Question
In math, the factorial of a number is defined as the product of an integer and all the integers below it. For example, the factorial of four (4!) is equal to 1x2x3x4=24. Fill in the blanks to make the factorial function return the right number.<br>
**Before:**
```
def factorial(n):
    result = 1
    for i in ___:
        __
    return result

print(factorial(4)) # should return 24
print(factorial(5)) # should return 120
```
**After:**
```
def factorial(n):
    result = 1
    for i in range(2,n+1):
        result *= i
    return result

print(factorial(4)) # should return 24
print(factorial(5)) # should return 120
```
### Nested for loops
```
for left in range(7):
    for right in range(left, 7):
        print("[" + str(left) + "|" + str(right) + "]", end=" ")
    print()
```
#### Question:
Given the following code, what should the next line be to avoid both variables being printed with the same value?
```
teams = [ 'Dragons', 'Wolves', 'Pandas', 'Unicorns']
for home_team in teams:
    for away_team in teams:
```
- [ ] while home_team != away_team:
- [ ] for home_team == away_team:
- [ ] away_team = home_team
- [x] if home_team != away_team:

>We want to print all possible team pairings but exclude those where a team would play against itself. To do that, we need a conditional that skips the case where both teams are the same.
```
teams = ["Dragons", "Wolves", "Pandas", "Unicorns"]
for home_team in teams:
    for away_team in teams:
        if home_team != away_team:
	    print(home_team + " vs " + away_team)
```
### Common errors in for loops
```
def greet_friends(friends):
    for friend in friends:
        print("Hi " + friend)

greet+friends(["Taylor", "Luisa", "Jamaal", "Eli"])
```
#### Question:
The validate_users function is used by the system to check if a list of users is valid or invalid. A valid user is one that is at least 3 characters long. For example, ['taylor', 'luisa', 'jamaal'] are all valid users. When calling it like in this example, something is not right. Can you figure out what to fix?<br>
**Before:**
```
def validate_users(users):
  for user in users:
    if is_valid(user):
      print(user + " is valid")
    else:
      print(user + " is invalid")

validate_users("purplecat")
```
**After:** (only change)
```
validate_users(["purplecat"])
```
## Recursion
### What is recursion?
A recursive function calls itself.
```
def factorial(n):
    if n < 2:
        return 1
    return n * factorial(n-1)
```
```
def factorial(n):
    print("Factorial called with " + str(n))
    if n < 2:
        print("Returning 1")
	return 1
    result = n * factorial(n-1)
    print("Returning " + str(result) + " for factorial of " + str(n))
    return result
    
factorial(4)
```
#### Question:
**Before**
```
def sum_positive_numbers(n):
    # The base case is n being smaller than 1
    if n < 1:
        return ___

    # The recursive case is adding this number to 
    # the sum of the numbers smaller than this one.
    return ___ + sum_positive_numbers(___)

print(sum_positive_numbers(3)) # Should be 6
print(sum_positive_numbers(5)) # Should be 15
```
**After:**
```
def sum_positive_numbers(n):
    if n == 1:
        return 1
    return n + sum_positive_numbers(n-1)

print(sum_positive_numbers(3)) # Should be 6
print(sum_positive_numbers(5)) # Should be 15
```

### Recursion in action in the IT context
