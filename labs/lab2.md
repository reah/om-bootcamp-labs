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
Now go ahead and save the file as `lab2.py` on your Desktop into a folder named `bootcamp`. As you can infer, the `.py` extension is used for files containing Python code.

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

This tells Python "I want to have a variable named `i`. The first value `i` will take on is 0. Now run the code underneath the for-loop header. Afer you are done running all of the code under it, give `i` its next value. `i` should take on the numbers that range from 0 upto (but not including) 20."

Let's go ahead and try this out. Open `lab2.py` in Sublime, clear out document, and type in the following:
```
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]

for i in range(0, 20):
    lst[i] = lst[i] * 2

print lst
```

Go back into Terminal, type `cd ~/Desktop/bootcamp` (no need to do this if you never closed Terminal) and then type `python lab2.py` You should now see that every value in `lst` has been multiplied by 2!

Here is another way of doing the same thing:
```
lst = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20]
new_lst = []

for val in lst:
    new_lst.append(val * 2)

lst = new_lst
print lst
```

Here, we don't use ranges or indices at all!

This is us telling Python "I want `val` to take on a new value with every iteration. The value `val` will take is the values in the list named `lst`. This means `val` will start at 1 since that is the first number in the list. Run the code under the for-loop header. After that, the next value `val` will take is 2 since it's the next number in `lst`. `val` will keep taking on new numbers until here are no numbers left in `lst`. Now, I want `lst` to equal the new list I appended all the doubled numbers into, called `new_lst`."

### While-Loops

## Functions
![Function](http://i.giphy.com/JkwGowOGUjy9y.gif)

## Watson API