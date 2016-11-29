# Day Two

## A New Way To Run Code
Last time we wrote commands directly into Terminal and Python responded immediately back to us, kind of like instant messenger. This is fine for the simple one line expressions we were writing like `4 * 8`. But now, we are going to take our skills to **THE NEXT LEVEL** so we'll be needing a better way to execute more complicated code.

![Next Level](http://i.giphy.com/VAqlxtQy2462I.gif)

*us going to the next level!!!*:fire::100:

### Sublime Text
Technically you can write code in any text editor, but a text editor specifically designed to handle code has some very handy tools that make life easier. The text editor we will be using in this course, and one that many programmers actually use, is called Sublime Text. Take a moment to download and install it it by clicking [here](https://download.sublimetext.com/Sublime%20Text%202.0.2.dmg).

### Doing The Deed

Now open Sublime Text (you can do this with Spotlight by pressing `command + space` and typing "Sublime"). Now you have a blank page ready for code. Let's write a simple program and see how we can run it. Type the following:
```
print "hello there"
```
Create a folder called `bootcamp` on your Desktop and save the file as `lab2.py` into that folder. As you can infer, the `.py` extension is used for files containing Python code.

Open Terminal now and type `cd ~/Desktop/bootcamp`. This isn't crucial to know, but `cd` stands for "change directories". We are telling Terminal to go into our Desktop and then into a folder called `bootcamp`. Now Terminal is "in" that folder and has acess to all the files in it. Type `ls` into Terminal and you should see all the files we have in `Desktop/bootcamp` (it should only be `lab2.py`)

In order to run the code now, all we have to do is type `python lab2.py`. That's it! This is how we can have Python execute code that we write in a file.

## Loops
*give a man a fish and you feed him for a day; teach a man to fish and you feed him for a lifetime* - Wiz Khalifa :100::100::100::100:

Suppose we had a list as such:
```
>>> lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]
```

and we wanted every element in `lst` to be multiplied by two
```
[2, 4, 6, 8, 10, 12, 14, 16, 18, 20, 22, 24, 26, 28, 30, 32, 34, 36, 38, 40]
```

As of now, there is no easy way to do this. We'd have to manually go into each element and type
```
>>> lst[0] = lst[0] * 2
>>> lst[1] = lst[1] * 2
>>> lst[2] = lst[2] * 2
>>> lst[3] = lst[3] * 2
.
.
.
etc.
```

![Patrick](http://i.giphy.com/l46CyJmS9KUbokzsI.gif)

That's what this guy would do. Don't be this guy.

This is where loops come in handy. As you can see, every operation here is very similar. If we could make a template for it, it would look something like this:
```
>>> lst[CURRENT NUMBER] = lst[CURRENT NUMBER] * 2
```

If this `CURRENT NUMBER` variable changed from 0 to 1 to 2 to 3 ... to 20 by itself, it would do the job for us.

### For-Loops
This is how you would approach that in Python:
```
for i in range(0, 20):
    lst[i] = lst[i] * 2
```

This tells Python the following:
* I want to have a variable named `i`
* The first value `i` will take on is 0
* Now run the code underneath the for-loop header
* Afer you are done running all of the code under it, give `i` its next value
* `i` should take on the numbers that range from 0 upto (but not including) 20

*The `0` in `range(0, 100)` is implied, so next time you can simply type `range(100)` unless you want to start at somewhere other than `0`. Also, most of the time we don't know exactly how long a list is, so we can type `range(len(lst))` to have Python iterate through the length of the list.*

Let's go ahead and try this out. Open `lab2.py` in Sublime, clear out document, and type in the following:
```
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]
print "BEFORE:", lst

for i in range(len(lst)):
    lst[i] = lst[i] * 2

print "AFTER:", lst
```

Go back into Terminal, type `cd ~/Desktop/bootcamp` (no need to do this if you never closed Terminal) and then type `python lab2.py` You should now see that every value in `lst` has been multiplied by 2!

Here is another way of doing the same thing. Go through each line and try to understand exactly what's happening and why this works. There are comments in there to guide you.
```
# Initializing lst to be the numbers from 1 to 20
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]
print "BEFORE:", lst

# Initializing and empty new list
new_lst = []

# For every value in lst
for val in lst:
    # Multiply the value by 2 and append it into the new list
    new_lst.append(val * 2)

# We don't need the old lst anymore, so replace it with new_lst
lst = new_lst
print "AFTER:", lst
```

Here, we don't use ranges or indices at all! In other words, we don't use `range` or have to even type `lst[i]`. We can directly bypass that step in Python by just typing `for VARIABLE in DATA STRUCTURE`.

*If that doesn't make sense maybe this explanation will help. Before, we were assigning `i` to be 0, 1, 2,...len(lst)-1 and then using `i` to access the elements in `lst` by using it as an index like `lst[i]`. Now, we are directly assigning `i` to the values in `lst`.*

Write this in Sublime, understand each line, and run it
```
fruits = {"apples": 5, "peaches": 1, "mangoes": 5, "strawberries": 7, "bananas": 2}

for key in fruits:
    print "The number of", key, "I have is", fruits[key]
    if key in ["apples", "mangoes", "bananas"]:
        print "I love", key, "so I bought one more!"
        fruits[key] = fruits[key] + 1
        print "Now I have", fruits[key], "of", key
```

Time for your first for-loop question. Open Sublime and start off with this code:
```
even = range(100)[::2]
odd = range(1, 100)[::2]
zipped = []
```

Here, `even` is 0, 2, 4, 6,...98 and `odd` is all 1, 3, 5, 9,...99. Now, we'd like `zipped` to be all the numbers from 0 to 99. How would you accomplish this using only 3 lines of code? *Hint: think about why it's called `zipped` and use a for-loop*

#### Extra Credit
How would you do that using only 2 lines of code?

#### Extra Extra Credit
How would you do that using just 1 line of code? (This is just a dumb trick question)

### While-Loops
For-loops are for instructions like "For every single element in a data structure, do this operation".

While-loops are good for instructions like "Keep doing an operation while a condition is true. Once it's false, stop doing that operation".

Here is a simple example of a while-loop:
```
i = 0

while i <  10:
    print "This is the current value", i
    i = i + 1

print "We are done and the value is", i
```

* Here, we start off a variable `i` at 0.
* Python then checks the while-condition which asks if `i` is less than 10.
* Python sees that `i = 0` which is indeed less than 10 so it proceeds to enter the while-loop.
* For every iteration of the while loop, it prints out the current value of `i` and increments it by 1. After each iteration, Python will check the while-condition again.
* Suppose we are at the iteration where `i = 9`. Now we check the while-condition. Yes, 9 is still less than 10.
* We then print out "This is the current value 9".
* Now we run `i = i + 1` so `i` equals 10 now.
* Now we go back up to the while-condition and check it to see if we keep continuing. `i = 10` which is *not* less than 10.
* Python immediately exits the while-loop **without printing out 10 inside the loop**
* Then finally we print, outside of the loop, what `i` is.

Don't write these out, just look at them with a partner and talk about what you think they print.
```
i = True
j = False

while i or j:
    i = not j
    j = i
    print i, j
```
```
i = 0
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]

while i < len(lst):
    lst[i] = lst[i] * 2
    i = i + 1

print lst
```
```
while True:
    print "Hello!"
```
```
i = 1
j = 20

while i < j:
    i = i * 2
    j = j + 1

print i, j
```

## Functions
![Function](http://i.giphy.com/JkwGowOGUjy9y.gif)

Functions in coding are just like functions in math; they have an input and an output. When you see `f(x) = x + 3` it's pretty clear what you're looking at. `f` is a function that takes an input `x`, add its by 3, and outputs it.

This is how you'd write that in Python:
```
def f(x):
    return x + 3
```

We'd call that function by typing `f(5)`. The `5` gets *passed into* the function as the *argument* `x` and the *return value* of the function is `8`. You could say `print f(5)` for example or say `var = f(5)` to store the *return value* in a variable.

Here are some other functions you can take a look at. Try to figure out what they'd output:
```
def f(x, y):
    return x * y
```
```
def f():
    return 5 * 5
```
```
def f(x, y):
    a = x ** y
    b = y ** x
    return a * b
```
```
def f(lst):
    new_lst = []

    for i in lst:
        new_lst.append(lst[i] + lst[i - 1])

    return new_lst
```
```
def f(x):
    return x * x

def g(x):
    return x + 3

print f(g(4))
```

### Nested Functions
![Functions](http://i.giphy.com/kOIbusN7fPnkk.gif)

Here is an example of a nested if-statement. Go through the whole thing and understand exactly what's going on and what it would output.
```
a = "heads"
b = "tails"
c = "heads"

if a == "heads":
    if b == "heads":
        if c == "heads":
            print "HHH"
        elif c == "tails":
            print "HHT"
    elif b == "tails":
        if c == "heads":
            print "HTH"
        elif c == "tails":
            print "HTT"
elif a == "tails":
    if b == "heads":
        if c == "heads":
            print "THH"
        elif c == "tails":
            print "THT"
    elif b == "tails":
        if c == "heads":
            print "TTH"
        elif c == "tails":
            print "TTT"
```

In a similar way, we can have functions within functions! Here is an example modeled off the [Pythaogrean theorem](https://en.wikipedia.org/wiki/Pythagorean_theorem):
```
def is_pythagorean(a, b, c):

    def square(x):
        return x ** 2

    return square(a) + square(b) == square(c)
```

What would `is_pythagorean(3, 4, 5)` output? How about `is_pythagorean(2, 5, 9)`?

#### Extra Credit
How can we write that 22 line heads/tails code above into a 10 line function? Think about how we can add strings together.

## Lab Work

![Work](http://i.giphy.com/l3uVRbeTOS6HTdFSw.gif)

1) Write a function that reverses a list and name it `reverse`.
```
>>> lst = [2, 6, 2, 4, 6, 8, 6, 5, 8, 9, 9, 9]
>>> reverse(lst)
[9, 9, 9, 8, 5, 6, 8, 6, 4, 2, 6, 2]
```

2) This exercise is a classic sotware engineering interview question. Write a function called `fizzbuzz` that prints the numbers from 0 to :100:. But for multiples of 3, print out "Fizz" instead of the number and for the multiples of 5, print out "Buzz". For numbers that are divisible by both 3 and 5, print out "FizzBuzz".
```
>>> fizzbuzz()
FizzBuzz
1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
16
17
Fizz
19
Buzz
Fizz
22
23
Fizz
Buzz
26
Fizz
28
29
FizzBuzz
31
32
Fizz
34
Buzz
Fizz
37
38
Fizz
Buzz
41
Fizz
43
44
FizzBuzz
46
47
Fizz
49
Buzz
Fizz
52
53
Fizz
Buzz
56
Fizz
58
59
FizzBuzz
61
62
Fizz
64
Buzz
Fizz
67
68
Fizz
Buzz
71
Fizz
73
74
FizzBuzz
76
77
Fizz
79
Buzz
Fizz
82
83
Fizz
Buzz
86
Fizz
88
89
FizzBuzz
91
92
Fizz
94
Buzz
Fizz
97
98
Fizz
Buzz
```

Congrats on finishing day 2!