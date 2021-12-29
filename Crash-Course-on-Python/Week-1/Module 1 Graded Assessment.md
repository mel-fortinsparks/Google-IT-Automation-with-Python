# Module 1 Graded Assessment
### Question 1: What is a computer program?
- [x] A step-by-step recipe of what needs to be done to complete a task, that gets executed by the computer. (Being able to write such programs is a super useful skill that you'll acquire through this course.)
- [ ] A file that gets printed by the Python interpreter.
- [ ] The syntax and semantics of Python.
- [ ] The overview of what the computer will have to do to solve some automation problem.
### Question 2: What’s automation?
- [x] The process of replacing a manual step with one that happens automatically. (By replacing a manual step with an automatic one we create automation that helps us reduce unnecessary manual work.)
- [ ] The inputs and outputs of a program.
- [ ] The checkout processes at a grocery store.
- [ ] The process of getting a haircut.
### Question 3: Which of the following tasks are good candidates for automation? Check all that apply.
- [x] Creating a report of how much each sales person has sold in the last month. (Creating reports based on data are a great example of things that can be automated.)
- [x] Setting the home directory and access permissions for new employees joining your company. (The process of setting up the account for a new employee is usually repetitive and most of it can be automated.)
- [x] Populating your company's e-commerce site with the latest products in the catalog. (Automatically populating a website based on data is a great example of a task that can be automated.)
- [ ] Writing a computer program.
- [ ] Designing the new webpage for your company.
- [ ] Taking pictures of friends and family at a wedding.
### Question 4: What are some characteristics of the Python programming language? Check all that apply.
- [x] Python programs are easy to write and understand. (Because the syntax used by Python is similar to the one used by the English language, Python programs are easy to write and understand.)
- [x] The Python interpreter reads our code and transforms it into computer instructions. (We write our code using Python's syntax and semantics, and the interpreter transforms that into instructions that our computer executes.)
- [x] We can practice Python using web interpreters or codepads as well as executing it locally. (We can practice writing Python code with many different tools available to us, both online and offline.)
- [ ] It's an outdated language that's barely in use anymore.
### Question 5: How does Python compare to other programming languages?
- [x] Each programming language has its advantages and disadvantages. (Each language has its pros and cons. The best language to choose will depend on the problem you are trying to solve.)
- [ ] Python is the only programming language that is worth learning.
- [ ] It's always better to use an OS specific language like Bash or Powershell than using a generic language like Python.
- [ ] Programming languages are so different that learning a second one is harder than learning the first one. 
### Question 6: Write a Python script that outputs "Automating with Python is fun!" to the screen.
```
print("Automating with Python is fun!")
```
### Question 7: Fill in the blanks so that the code prints "Yellow is the color of sunshine".
```
color = "Yellow"*
thing = "sunshine"*
print(color + " is the color of " + thing)*
```
### Question 8: Keeping in mind there are 86400 seconds per day, write a program that calculates how many seconds there are in a week, if a week is 7 days.  Print the result on the screen.
**Note: Your result should be in the format of just a number, not a sentence.**
```
secondsperwk = 86400*7
print(secondsperwk)
```
### Question 9: Use Python to calculate how many different passwords can be formed with 6 lower case English letters.  For a 1 letter password, there would be 26 possibilities.  For a 2 letter password, each letter is independent of the other, so there would be 26 times 26 possibilities.  Using this information, print the amount of possible passwords that can be formed with 6 letters.
```
numpass = 26*26*26*26*26*26
print(numpass)
```
### Question 10: Most hard drives are divided into sectors of 512 bytes each.  Our disk has a size of 16 GB. Fill in the blank to calculate how many sectors the disk has.
**Note: Your result should be in the format of just a number, not a sentence.**
```
disk_size = 16*1024*1024*1024
sector_size = 512
sector_amount = disk_size/sector_size

print(sector_amount)
```
