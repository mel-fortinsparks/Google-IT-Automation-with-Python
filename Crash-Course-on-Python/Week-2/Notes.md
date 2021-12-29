## Functions
### Function written to calculate the total number of seconds for a time period
Flesh out the body of the print_seconds function so that it prints the total amount of seconds given the hours, minutes, and seconds function parameters. Remember that there are 3600 seconds in an hour and 60 seconds in a minute.
<br><br>**Before:**
```
def print_seconds(hours, minutes, seconds):
    print(___)

print_seconds(1,2,3)
```
**After:**
```
def print_seconds(hours, minutes, seconds):
    print(3600*hours+60*minutes+seconds)

print_seconds(1,2,3)
```

### Function written to add together two functions with the number of seconds in a time period
Use the get_seconds function to work out the amount of seconds in 2 hours and 30 minutes, then add this number to the amount of seconds in 45 minutes and 15 seconds. Then print the result.
<br><br>**Before:**
```
def get_seconds(hours, minutes, seconds):
  return 3600*hours + 60*minutes + seconds

amount_a = get_seconds(___)
amount_b = get_seconds(___)
result = ___
print(result)
```
**After:**
```
def get_seconds(hours, minutes, seconds):
  return 3600*hours + 60*minutes + seconds

amount_a = get_seconds(2,30,0)
amount_b = get_seconds(0,45,15)
result = amount_a + amount_b
print(result)
```
### Function written to reduce duplication
In this code, identify the repeated pattern and replace it with a function called month_days, that receives the name of the month and the number of days in that month as parameters. Adapt the rest of the code so that the result is the same. Confirm your results by making a function call with the correct parameters for both months listed.
<br><br>**Before:**
```
# REPLACE THIS STARTER CODE WITH YOUR FUNCTION
june_days = 30
print("June has " + str(june_days) + " days.")
july_days = 31
print("July has " + str(july_days) + " days.")
```
**After:**
```
def month_days(month, days):
    print(month+" has " + str(days) + " days.")
month_days("June", 30)
month_days("July", 31)
```
### This is the solution to the old question for the same video:
```
def print_monthly_expense(month, hours):
    total = hours * 0.65
    print("In " + month + " we spent: " + str(total))
print_monthly_expense("June", 243)
print_monthly_expense("July", 325)
print_monthly_expense("August", 298)
```
### Write a fuction to calculate the area of a rectanger that is more readable
This function to calculate the area of a rectangle is not very readable. Can you refactor it, and then call the function to calculate the area with base of 5 and height of 6?
>Tip: a function that calculates the area of a rectangle should probably be called rectangle_area, and if it's receiving base and height, that's what the parameters should be called.
<br><br>**Before:**
```
def f1(x, y):
	z = x*y  # the area is base*height
	print("The area is " + str(z))
```
**After:**
```
def rectangle_area(base, height):
	area = base*height  # the area is base*height
	print("The area is " + str(area))

rectangle_area(5,6)
```
## Conditionals
The is_positive function should return True if the number received is positive, otherwise it returns None. Can you fill in the gaps to make that happen?
<br><br>**Before:**
```
def is_positive(number):
  if ___:
    return ___
```
**After:**
```
def is_positive(number):
  if number > 0:
    return True
  else:
    return
```
The number_group function should return "Positive" if the number received is positive, "Negative" if it's negative, and "Zero" if it's 0. Can you fill in the gaps to make that happen?
<br><br>**Before:**
```
def number_group(number):
  if ___:
    return "Positive"
  elif ___:
    return ___
  else:
    ___
```
**After:**
```
def number_group(number):
  if number > 0:
    return "Positive"
  elif number == 0:
    return "Zero"
  else:
    return "Negative"
```
