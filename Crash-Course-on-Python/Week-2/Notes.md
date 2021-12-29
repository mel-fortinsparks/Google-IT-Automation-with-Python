
#### Function written to calculate the total number of seconds for a time period
**Before:**
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
