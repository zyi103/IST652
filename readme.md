# IST 652 Lab #1
### Instructions
- Complete all 6 questions in this assignment.
- You may work with others, <b> but the work you submit must be your own </b>.
You can differentiate your work by adding comments or changing the values you
use to test your code. However, submitting some else's work as your own is an
academic integrity violation and will be raised to academic affairs.
- It is always better to attempt a problem as partial credit may be granted.


### Submission Guide:
- Submit your answers on BlackBoard by Saturday 2019-02-02.
- The file must be .ipynb file type.
- The name of the file should be <i> ist652_lab1_lastname.ipynb </i> .


### Grading [ 6 total points ]
For Each Question, the following credit will be awarded:
- 0.75 for printing the correct answer to the console.
- 0.15 for approaching the problem efficiently.
- 0.10 for properly documenting and commenting your code.

---
### Questions

#### ( 1 ) Write the following code and return <i>x</i> using the print
function. What does it return and why?
- x = 11110
- x = x+1

##### [1 point]

```{.python .input  n=1}
# Enter your code here, printing relevant answers to console:
x = 11110
x = x + 1
print(x)

# [1] 11111
# x will return 11111 because we first assigned x to be 11110 then we did + 1, which equal to 11111


```

```{.json .output n=1}
[
 {
  "name": "stdout",
  "output_type": "stream",
  "text": "11111\n"
 }
]
```

----
#### ( 2 ) Assume that we execute the following assignment statements:
- width = 17
- height = 12.0

#### For each of the following expressions, print the value of the expression
and its data type.
-  width / 2
-  width / 2.0
-  height * 2
-  height / 2.0
-  width / height


##### [1 point]

```{.python .input  n=8}
# Enter your code here, printing relevant answers to console:

width = 17
height = 12.0

print(width / 2, type(width / 2))
print(width / 2.0, type(width / 2.0))
print(height * 2, type(height * 2))
print(height / 2.0, type(height / 2.0))
print(width / height, type(width / height))


```

```{.json .output n=8}
[
 {
  "name": "stdout",
  "output_type": "stream",
  "text": "8.5 <class 'float'>\n8.5 <class 'float'>\n24.0 <class 'float'>\n6.0 <class 'float'>\n1.4166666666666667 <class 'float'>\n"
 }
]
```

---
#### ( 3 ) Write a sequence of statements which <u><i>prompt</i></u> the user
for hours and rate per hour, printing each one, and then to computing gross pay
as:
- ( hours * rate )

#### Your output lines should look something like:
- Enter Hours: 35
- Enter Rate: 2.75
- Pay: 96.25


##### [1 point]

```{.python .input  n=15}
# Enter your code here, printing relevant answers to console:

hrs = float(input("Enter Hours: "))
rate = float(input("Enter Rate: "))
print("Pay: ", hrs * rate)




```

```{.json .output n=15}
[
 {
  "name": "stdout",
  "output_type": "stream",
  "text": "Enter Hours: 2 \nEnter Rate: 23\nPay:  46.0\n"
 }
]
```

 ----

#### ( 4 ) Rewrite your pay computation <i><u>(#3)</u></i> to give the employee
1.5 times the hourly rate for hours worked above 40 hours.
#### For example:
- Hours: 45
- Rate: 10
- Pay: 475.0


##### [1 point]

```{.python .input  n=40}
# Enter your code here, printing relevant answers to console:

hrs = float(input("Enter Hours: "))
rate = float(input("Enter Rate: "))
print("Pay: ", hrs * rate + (0 if (hrs < 40) else (hrs - 40) * 1.5))


```

```{.json .output n=40}
[
 {
  "name": "stdout",
  "output_type": "stream",
  "text": "Enter Hours: 50\nEnter Rate: 1\nPay:  65.0\n"
 }
]
```

---

#### ( 5 ) Suppose that there is a list of strings defined, called samples.
Define the list so that some strings have only 1 or 2 characters and some
strings have more.  Write a loop that prints out all the strings whose length is
greater than 2.

Nake up a list then write your loop to use the list samples, for example:

   <i> samples = [‘at’, ‘bat’, ‘c’, . . . .  ]  </i>

Submit your list, your code and an example run.


##### [1 point]

```{.python .input  n=45}
# Enter your code here, printing relevant answers to console:

samples = ['java', 'python', 'C', 'go', 'js', 'ruby', 'C#', 'PHP']

for string in samples:
    if len(string) > 2:
        print(string)


```

```{.json .output n=45}
[
 {
  "name": "stdout",
  "output_type": "stream",
  "text": "java\npython\nruby\nPHP\n"
 }
]
```

#### ( 6 ) Again suppose that there is a list of strings defined, called
samples.  Define the list so that some strings have only 1 or 2 characters and
some strings have <u>more than 5.</u>  Write a loop that prints out all the
strings whose length is greater than 2 and whose length is less than 5.

Make up a list then write your loop to use the list samples. For example:

<i>samples = [‘at’, ‘book’, ‘c’, ‘dog’, ‘elephant’, . . .  ]</i>

Submit your list, your code and an example run.


##### [1 point]

```{.python .input  n=52}
# Enter your code here, printing relevant answers to console:

samples = ['java', 'python', 'C', 'go', 'js', 'ruby', 'C#', 'PHP']

for string in samples:
    if len(string) > 2 and len(string) < 5:
        print(string)

#question unclear here is solution 2
greaterThanTwo = []
lessThanFive = []
for string in samples:
    if len(string) > 2:
        greaterThanTwo.append(string)
    if len(string) < 5:
        lessThanFive.append(string)
    
print("Strings thats Greater Than Two:", *greaterThanTwo)
print("Strings thats Less Than Five:", *lessThanFive)    



```

```{.json .output n=52}
[
 {
  "name": "stdout",
  "output_type": "stream",
  "text": "java\nruby\nPHP\nStrings thats Greater Than Two: java python ruby PHP\nStrings thats Less Than Five: java C go js ruby C# PHP\n"
 }
]
```
