
### Function written to calculate the total number of seconds for a time period
Flesh out the body of the print_seconds function so that it prints the total amount of seconds given the hours, minutes, and seconds function parameters. Remember that there are 3600 seconds in an hour and 60 seconds in a minute.
<br>**Before:**
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
<br>**Before:**
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
