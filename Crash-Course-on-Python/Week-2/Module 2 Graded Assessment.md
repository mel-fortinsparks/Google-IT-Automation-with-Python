# Module 2 Graded Assessment
### Question 1: Complete the function by filling in the missing parts. The color_translator function receives the name of a color, then prints its hexadecimal value. Currently, it only supports the three additive primary colors (red, green, blue), so it returns "unknown" for all other colors.
**Before**
```
def color_translator(color):
	if ___ == "red":
		hex_color = "#ff0000"
	elif ___ == "green":
		hex_color = "#00ff00"
	elif ___ == "blue":
		hex_color = "#0000ff"
	___:
		hex_color = "unknown"
	return ___
```
**After:**
```
def color_translator(color):
	if color == "red":
		hex_color = "#ff0000"
	elif color == "green":
		hex_color = "#00ff00"
	elif color == "blue":
		hex_color = "#0000ff"
	else:
		hex_color = "unknown"
	return hex_color
```
>print(color_translator("blue")) # Should be #0000ff <br>
>print(color_translator("yellow")) # Should be unknown<br>
>print(color_translator("red")) # Should be #ff0000<br>
>print(color_translator("black")) # Should be unknown<br>
>print(color_translator("green")) # Should be #00ff00<br>
>print(color_translator("")) # Should be unknown <br>
 
### Question 2: What's the value of this Python expression: "big" > "small"
- [ ] True
- [x] False
- [ ] big
- [ ] small
>The conditional operator > checks if two values are equal. The result of that operation is a boolean: either True or False. Alphabetically, "big" is less than "small".
### Question 3: 
- [ ] To mark the end of the if statement
- [x] To handle more than two comparison cases
- [ ] To replace the "or" clause in the if statement
- [ ] Nothing - it's a misspelling of the else-if keyword
>The elif keyword is used in place of multiple embedded if clauses, when a single if/else structure is not enough.
### Question 4: 
**Before:**
```
def exam_grade(score):
	if ___:
		grade = "Top Score"
	elif ___:
		grade = "Pass"
	else:
		grade = "Fail"
	return grade
```
**After:**
```
def exam_grade(score):
	if score>95:
		grade = "Top Score"
	elif score>=60:
		grade = "Pass"
	else:
		grade = "Fail"
	return grade
```
>print(exam_grade(65)) # Should be Pass<br>
>print(exam_grade(55)) # Should be Fail<br>
>print(exam_grade(60)) # Should be Pass<br>
>print(exam_grade(95)) # Should be Pass<br>
>print(exam_grade(100)) # Should be Top Score<br>
>print(exam_grade(0)) # Should be Fail<br>
### Question 5: What's the value of this Python expression: 11 % 5?
- [ ] 2.2
- [ ] 2
- [x] 1
- [ ] 0
>"%" is the modulo operator, which returns the remainder of the integer division between two numbers. 11 divided by 5 equals 2 with remainder of 1.
### Question 6: Complete the body of the format_name function. This function receives the first_name and last_name parameters and then returns a properly formatted string.
Specifically: 
- If both the *last_name* and the *first_name* parameters are supplied, the function should return like so:
```
print(format_name("Ella", "Fitzgerald"))
Name: Fitzgerald, Ella
```
- If only one name parameter is supplied (either the first name or the last name) , the function should return like so:
```
print(format_name("Adele", ""))
Name: Adele
```
- Finally, if both names are blank, the function should return the empty string:
```
print(format_name("", "Einstein"))
Name: Einstein
```
**Before:**
```
def format_name(first_name, last_name):
	# code goes here
	
	return string 
```
**After:**
```
def format_name(first_name, last_name):
	# code goes here
	if first_name=="" and last_name=="":
		string=""
	elif first_name=="":
		string= "Name: "+last_name
	elif last_name=="":
		string= "Name: "+first_name
	else:
		string= "Name: "+last_name+", "+first_name
	return string 
```
>print(format_name("Ernest", "Hemingway")) # Should return the string "Name: Hemingway, Ernest" <br>
>print(format_name("", "Madonna")) # Should return the string "Name: Madonna"<br>
>print(format_name("Voltaire", "")) # Should return the string "Name: Voltaire"<br>
>print(format_name("", "")) # Should return an empty string<br>
### Question 7: The longest_word function is used to compare 3 words. It should return the word with the most number of characters (and the first in the list when they have the same length). Fill in the blank to make this happen.
**Before:**
```
def longest_word(word1, word2, word3):
	if len(word1) >= len(word2) and len(word1) >= len(word3):
		word = word1
	elif ___:
		word = word2
	else:
		word = word3
	return(word)

print(longest_word("chair", "couch", "table"))
print(longest_word("bed", "bath", "beyond"))
print(longest_word("laptop", "notebook", "desktop"))
```
**After:**
```
def longest_word(word1, word2, word3):
	if len(word1) >= len(word2) and len(word1) >= len(word3):
		word = word1
	elif len(word2) >= len(word1) and len(word2) >=len(word3):
		word = word2
	else:
		word = word3
	return(word)
```
### Question 8: What’s the output of this code?
```
def sum(x, y):
		return(x+y)
print(sum(sum(1,2), sum(3,4)))
```
**Output: 10**
### Question 9: What's the value of this Python expression?
```
((10 >= 5*2) and (10 <= 5*2))
```
- [x] True
- [ ] False
- [ ] 10
- [ ] 5x2
### Question 10: The fractional_part function divides the numerator by the denominator, and returns just the fractional part (a number between 0 and 1). Complete the body of the function so that it returns the right number.
Note: Since division by 0 produces an error, if the denominator is 0, the function should return 0 instead of attempting the division.
<br>**Before:**
```
def fractional_part(numerator, denominator):
	# Operate with numerator and denominator to 
# keep just the fractional part of the quotient
	return 0
```
**After:**
```
def fractional_part(numerator, denominator):
	if numerator==0:
		return 0
	elif denominator==0:
		return 0
	else:
		return (numerator/denominator)-(numerator//denominator)
```
>print(fractional_part(5, 5)) # Should be 0
>print(fractional_part(5, 4)) # Should be 0.25
>print(fractional_part(5, 3)) # Should be 0.66...
>print(fractional_part(5, 2)) # Should be 0.5
>print(fractional_part(5, 0)) # Should be 0
>print(fractional_part(0, 5)) # Should be 0
