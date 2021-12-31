# Strings
### String Indexing and Slicing
>String indexing allows you to access individual characters in a string. You can do this by using square brackets and the location, or index, of the character you want to access. It's important to remember that Python starts indexes at 0. So to access the first character in a string, you would use the index [0]. If you try to access an index that’s larger than the length of your string, you’ll get an IndexError. This is because you’re trying to access something that doesn't exist! You can also access indexes from the end of the string going towards the start of the string by using negative values. The index [-1] would access the last character of the string, and the index [-2] would access the second-to-last character.
>
>You can also access a portion of a string, called a slice or a substring. This allows you to access multiple characters of a string. You can do this by creating a range, using a colon as a separator between the start and end of the range, like [2:5]. 
>
>This range is similar to the range() function we saw previously. It includes the first number, but goes to one less than the last number. For example:
>
```
fruit = "Mangosteen"
fruit[1:4]
```
>'ang'
>
>The slice includes the character at index 1, and excludes the character at index 4. You can also easily reference a substring at the start or end of the string by only specifying one end of the range. For example, only giving the end of the range:
>
```
fruit[:5]
```
>'Mango'
>
>This gave us the characters from the start of the string through index 4, excluding index 5. On the other hand this example gives is the characters including index 5, through the end of the string:
```
fruit[5:]
```
>'steen'
>
>You might have noticed that if you put both of those results together, you get the original string back!
```
>>> fruit[:5] + fruit[5:]
```
>'Mangosteen'
>
>Cool!

### Basic String Methods
>In Python, strings are immutable. This means that they can't be modified. So if we wanted to fix a typo in a string, we can't simply modify the wrong character. We would have to create a new string with the typo corrected. We can also assign a new value to the variable holding our string.
>
>If we aren't sure what the index of our typo is, we can use the string method *index* to locate it and return the index. Let's imagine we have the string **"lions tigers and bears"** in the variable **animals**. We can locate the index that contains the letter **g** using *animals.index("g")*, which will return the index; in this case 8. We can also use substrings to locate the index where the substring begins. *animals.index("bears")* would return 17, since that’s the start of the substring. If there’s more than one match for a substring, the index method will return the first match. If we try to locate a substring that doesn't exist in the string, we’ll receive a **ValueError** explaining that the substring was not found.
>
>We can avoid a **ValueError** by first checking if the substring exists in the string. This can be done using the *in* keyword. We saw this keyword earlier when we covered *for* loops. In this case, it's a conditional that will be either True or False. If the substring is found in the string, it will be True. If the substring is not found in the string, it will be False. Using our previous variable **animals**, we can do **"horses" in animals** to check if the substring "horses" is found in our variable. In this case, it would evaluate to False, since horses aren’t included in our example string. If we did **"tigers" in animals**, we'd get True, since this substring is contained in our string.

### Advanced String Methods

### String Formatting


# Lists
### For Loops Recap
>*For* loops allow you to iterate over a sequence of values. Let's take the example from the beginning of the video:
```
for x in range(5):
  print(x)
```
>Similar to *if* statements and *while* loops, *for* loops begin with the keyword *for* with a colon at the end of the line. 
>Just like in function definitions, *while* loops and *if* statements, the body of the *for* loop begins on the next line and is indented to the right. 
>But what about the stuff in between the *for* keyword and the colon? In our example, we’re using the *range()* function to create a sequence of numbers 
>that our *for* loop can iterate over. In this case, our variable x points to the current element in the sequence as the *for* loop iterates over the 
>sequence of numbers. Keep in mind that in Python and many programming languages, a range of numbers will start at 0, and the list of numbers generated 
>will be one less than the provided value. So *range(5)* will generate a sequence of numbers from 0 to 4, for a total of 5 numbers.
>
>Bringing this all together, the *range(5)* function will create a sequence of numbers from 0 to 4. Our *for* loop will iterate over this sequence of numbers, 
>one at a time, making the numbers accessible via the variable x and the code within our loop body will execute for each iteration through the sequence. 
>So for the first loop, x will contain 0, the next loop, 1, and so on until it reaches 4. Once the end of the sequence comes up, the loop will exit and the code will continue.
>
>The power of *for* loops comes from the fact that it can iterate over a sequence of any kind of data, not just a range of numbers. You can use *for* loops to iterate 
>over a list of strings, such as usernames or lines in a file.
>
>Not sure whether to use a *for* loop or a *while* loop? Remember that a *while* loop is great for performing an action over and over until a condition has changed. 
>A *for* loop works well when you want to iterate over a sequence of elements.  

### A Closer Look at the Range() Function
>Previously we had used the *range()* function by passing it a single parameter, and it generated a sequence of numbers from 0 to one less than we specified. 
>But the *range()* function can do much more than that. We can pass in two parameters: the first specifying our starting point, the second specifying the end point. 
>Don't forget that the sequence generated won't contain the last element; it will stop one before the parameter specified.
>
>The *range()* function can take a third parameter, too. This third parameter lets you  alter the size of each step. So instead of creating a sequence of numbers 
>incremented by 1, you can generate a sequence of numbers that are incremented by 5.
>
>To quickly recap the *range()* function when passing one, two, or three parameters:
> - One parameter will create a sequence, one-by-one, from zero to one less than the parameter.
> - Two parameters will create a sequence, one-by-one, from the first parameter to one less than the second parameter.
> - Three parameters will create a sequence starting with the first parameter and stopping before the second parameter, but this time increasing each step by the third parameter.

### Loops Cheat Sheet
> #### Loops Cheat Sheet
>Check out below for a run down of the syntax for while loops and for loops.
>
> #### While Loops
>A while loop executes the body of the loop while the condition remains True.<br>
>Syntax:
```
while condition:
    body
```
>**Things to watch out for!**
> - **Failure to initialize variables.** Make sure all the variables used in the loop’s condition  are initialized before the loop.
> - **Unintended infinite loops.** Make sure that the body of the loop modifies the variables used in the condition, so that the loop 
> will eventually end **for all possible values of the variables.**
>
>Typical use:<br>
>While loops are mostly used when there’s an unknown number of operations to be performed, and a condition needs to be checked at each iteration.
>
> #### For Loops
>A for loop iterates over a sequence of elements, executing the body of the loop for each element in the sequence.<br>
>Syntax:
```
for variable in sequence
    body
```
>The range() function:
>range() generates a sequence of integer numbers. It can take one, two, or three parameters:
> - range(n): 0, 1, 2, ... n-1
> - range(x,y): x, x+1, x+2, ... y-1
> - range(p,q,r): p, p+r, p+2r, p+3r, ... q-1 (if it's a valid increment)
>**Common pitfalls:**
> - **Forgetting that the upper limit of a range() isn’t included.**
> - **Iterating over non-sequences.** Integer numbers aren’t iterable. Strings are iterable letter by letter, but that might not be what you want.
> 
>Typical use:<br>
>For loops are mostly used when there's a pre-defined sequence or range of numbers to iterate.
>
> #### Break & Continue
>You can interrupt both while and for loops using the break keyword. We normally do this to interrupt a cycle due to a separate condition.
>
>You can use the continue keyword to skip the current iteration and continue with the next one. This is typically used to jump ahead when some of the elements of the sequence aren’t relevant.
>
>If you want to learn more, check out this wiki page on for loops. https://wiki.python.org/moin/ForLoop

# Dictionaries
### Additional Recursion Sources
>In the past videos, we visited the basic concepts of recursive functions.
>
>A recursive function must include a recursive case and base case. The recursive case calls the function again, with a different value. The base case returns a value without calling the same function.
>
>A recursive function will usually have this structure:
```
def recursive_function(parameters):
    if base_case_condition(parameters):
        return base_case_value
    recursive_function(modified_parameters)
```
>For more information on recursion, check out these resources:
> - Wikipedia Recursion page https://en.wikipedia.org/wiki/Recursion
> - See what happens when you Search Google for Recursion https://www.google.com/search?q=recursion
