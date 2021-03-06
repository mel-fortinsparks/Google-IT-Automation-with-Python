## Strings
### What is a string?
#### Question: 
Modify the double_word function so that it returns the same word repeated twice, followed by the length of the new doubled word. For example, double_word("hello") should return hellohello10.<br>
**Before:**
```
def double_word(word):
    return

print(double_word("hello")) # Should return hellohello10
print(double_word("abc"))   # Should return abcabc6
print(double_word(""))      # Should return 0
```
**After:**
```
def double_word(word):
    return word*2 + str(len(word*2))

print(double_word("hello")) # Should return hellohello10
print(double_word("abc"))   # Should return abcabc6
print(double_word(""))      # Should return 0
```
**Output:**
```
hellohello10
abcabc6
0
```
### The parts of a string
```
name = "Jaylen"
print(name[1])
```
Output:
```
a
```
>The first letter, J, is in the "0" position); Python starts counting indexes from 0, not one.
```
print(name[0])
print(name[5])
```
Output:
```
J
n
```
If you do print(name[6]), it'll give you a traceback error because it is outside of the range of the given string. If you don't know how long a string is, you can use negative indexes instead.
```
text = "Random string with a lot of characters"
print(text[-1])
print(text[-2])
```
Output:
```
s
r
```
#### Question
Want to give it a go yourself? Be my guest! Modify the first_and_last function so that it returns True if the first letter of the string is the same as the last letter of the string, False if they’re different. Remember that you can access characters using message[0] or message[-1].<br><br>
Be careful how you handle the empty string, which should return True since nothing is equal to nothing.<br>
**Before:**
```
def first_and_last(message):
    return False

print(first_and_last("else"))
print(first_and_last("tree"))
print(first_and_last(""))
```
**After:**
```
def first_and_last(message):
    if message =="":
        return True
    if message[0] == message[-1]:
        return True
    if message[0] != message[-1]:
        return False

print(first_and_last("else"))
print(first_and_last("tree"))
print(first_and_last(""))
```
**Output:**
```
True
False
True
```

### Creating new strings
#### Question
Using the index method, find out the position of "x" in "supercalifragilisticexpialidocious".
```
word = "supercalifragilisticexpialidocious"
print(word.index("x"))
```
Notes:
```
def replace_domain(email, old_domain, new_domain):
    if "@" + old_domain in email:
        index = email.index("@" + old_domain)
        new_email = email[:index] + "@" + new_domain
        return new_email
    return email
```
### More string methods
#### Question
Fill in the gaps in the initials function so that it returns the initials of the words contained in the phrase received, in upper case. For example: "Universal Serial Bus" should return "USB"; "local area network" should return "LAN”.
<br>**Before:**
```
def initials(phrase):
    words = phrase.___
    result = ""
    for word in words:
        result += ___
    return ___

print(initials("Universal Serial Bus")) # Should be: USB
print(initials("local area network")) # Should be: LAN
print(initials("Operating system")) # Should be: OS
```
**After:**
```
def initials(phrase):
    words = phrase.split()
    result = ""
    for word in words:
        result += word[0]
    return result.upper()

print(initials("Universal Serial Bus")) # Should be: USB
print(initials("local area network")) # Should be: LAN
print(initials("Operating system")) # Should be: OS
```
### Formatting strings
#### Question
```
name = "Manny"
number = len(name) * 3
print("Hello {}, your lucky number is {}".format(name,number))
```
```
print("Your lucky number is {number}, {name}.".format(name=name, number=len(name)*3))
```
Modify the student_grade function using the format method, so that it returns the phrase "X received Y% on the exam". For example, student_grade("Reed", 80) should return "Reed received 80% on the exam".
<br>**Before:**
```
def student_grade(name, grade):
	return ""

print(student_grade("Reed", 80))
print(student_grade("Paige", 92))
print(student_grade("Jesse", 85))
```
**After:**
```
def student_grade(name, grade):
	return "{name} received {grade}% on the exam".format(name=name, grade=grade)

print(student_grade("Reed", 80))
print(student_grade("Paige", 92))
print(student_grade("Jesse", 85))
```
More Notes:
```
price = 7.5
with_tax = price * 1.09
print("Base price: ${:.2f}. With tax: ${:.2f}.".format(price, with_tax))
```
## Lists
### What is (a list)?
#### Question
Fill in the gaps of the .<br>
**Before**
```

```
**After:**
```

```
### Modifying the contents of a list
#### Question
In math, the factorial of .<br>
**Before:**
```

```
**After:**
```

```
### Lists and tuples
#### Question:
Given the following code,?
```

```
- [ ] while home_team != away_team:
- [ ] for home_team == away_team:
- [ ] away_team = home_team
- [x] if home_team != away_team:

>We want to print 

### Iterating over lists and tuples
#### Question:
The validate_users functio<br>
**Before:**
```

```
**After:** 
```

```
### List comprehensions
#### Question
The following code 
<br>**Before:**
```

```
**After:**
```

```
## Dictionaries
### What is a dictionary?
#### Question
The following code 
<br>**Before:**
```

```
**After:**
```

```
### Iterating over the contents of a dictionary
#### Question:
**Before**
```

```
**After:**
```

```

### Dictionaries vs lists
#### Question
The following code 
<br>**Before:**
```

```
**After:**
```

```
