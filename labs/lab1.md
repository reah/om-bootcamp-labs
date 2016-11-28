# Day One

## Introduction to Terminal

![Terminal](https://media.giphy.com/media/1230rTAtEjLyLu/giphy.gif)

Terminal is a tool you use to give the computer commands to run. It's generally used to run quick commands and not type whole bodies of code. It's analogous to sending an instant message versus sending an email.

### Accessing Terminal
Go to Finder > Applications > Utilities > Terminal

Or, alternatively, press `command + space` to open Spotlight and type in "Terminal"

### Accessing Python
In terminal, type `python` and press enter. Literally that's it. Now you've opened a conversation with Python. The `>>>` you see is Python's way of saying it's ready for you to enter a command. Go ahead and type `>>> print "Hello World!"` and press enter.

Congrats, you've written your first program!

## Introduction to Python
![Python](https://www.python.org/static/opengraph-icon-200x200.png)
### Simple Arithmetic
Try typing the following commands into Python and press enter. Try to figure out what they are doing with a partner. Some of them are straight-forward and some of them are a *little* tricky.

*Do not copy and paste, type each command yourself. Remember, you have to enter each command EXACTLY as it appears*
```
>>> 2 + 3
>>> 2 * 3
>>> (2 + 3) * (2 * 3)
>>> a = 2 + 3
>>> a + (2 * 3)
>>> 2 ** 3
>>> 2 / 3
>>> 3 / 3
>>> 7 / 3
>>> 2.0 / 3
>>> 7 / 3.0
>>> 1 % 4
>>> 3 % 4
>>> 4 % 4
>>> 5 % 4
>>> 8 % 4
>>> 11 % 4
>>> (((2 + 3) * (2 * 3 ** 2)) / 3.0) % 4
>>> a = 2 + 3
>>> b = 2 * 3 ** 2
>>> c = 3.0
>>> d = 4
>>> ((a * b) / c) % d
>>> "Hello" + " " + "World!"
>>> c = 2 * 4
>>> print "If you multiply", 2, "and", 1 + 3, "you get", c
>>> 2 / 0
```

### Boolean Operators
*To be or not to be, that is the question...*

These are tools used to answer questions about equality. Try the following out:
```
>>> a = 4
>>> b = 4
>>> a == b
>>> a == 5
>>> a + b == 8
>>> a < 4
>>> a > 4
>>> a <= 4
>>> None == None
>>> "b" < "c"
>>> "ibm" > "google"
>>> "reah" > "anand"
```
While I disagree with the last one, you get the idea. You can use these operators on more than just numbers.

#### Logic
*Remember, ALL parts must be True for an `and` statement to be true and ONLY ONE part must be True for an `or` statement to be true*.

To save you from typing "True" and "False" everytime, just assign them to variables.
```
>>> t = True
>>> f = False
>>> t and t
>>> t and f
>>> t or f
>>> f or f
>>> not t
>>> not f == t
>>> t and t and t and t and f
>>> f or f or f or f or t
>>> t and f or f or t
>>> (t and f) or (f or t)
```

### Conditionals
Now that we have an idea of how booleans work, we can try using them to make computers complete simple logical tasks. Try the following out. Remember, you must press TAB everywhere you see a long space. You will see the Terminal output a `...`, that indicates that Python is now *in* the if statement. After finishing the statement, you will see one final `...` and you just have to press enter to finish your statement.
```
>>> a = 5
>>> b = 10
>>> c = 20
>>> if a + b > c:
...     print "Woohoo!"
... elif a + b == c:
...     print "Yayay!"
... else:
...     print "Bravo!"
...
```
Try this one out too:
```
>>> j = None
>>> k = 100
>>> if j and k:
...     print "JK!!!"
... elif j or k:
...     print "woohoo!"
... elif j:
...     print "j!!!"
... elif k:
...     print "K!!!"
...
```

## Data Structures
To swim, you use a pool.

To drink, you use a glass.

To spray, you use a hose.

To boil, water you use a pot.

Even though it's all the same water, your *purpose* determines the vessel you use to contain it. Similarly, data is like water - young padawan. There are many ways to store it depending on what you want to do with it. We will be covering two of these *data structures*.

### Lists
Try the following out. Some of the statements you run won't output anything.
```
>>> kp = []
>>> kp.append("top bun")
>>> kp.append("secret sauce")
>>> kp.append("krabby patty")
>>> kp.append("chum")
>>> kp.append("veggies")
>>> kp.append("bottom bun")
>>> kp
>>> kp[0]
>>> kp[1]
>>> kp[2]
>>> kp[-1]
>>> kp[-2]
>>> len(kp)
>>> kp[len(kp)]
>>> kp[len(kp) - 1]
>>> kp[-1] == kp[len(kp) - 1]
>>> kp.index("krabby patty")
>>> kp.count("chum")
>>> kp.remove("chum")
>>> kp.count("chum")
>>> seq = [5, 7, 1, 2, 8, 9, 0, 3, 4, 6]
>>> seq.sort()
>>> seq
>>> seq[:5]
>>> seq[5:]
>>> seq[::2]
>>> list_of_lists = [[1, 2, 3], [4, 5, 6], [[False], [], ["hello", 7]]]
>>> list_of_lists[1]
>>> list_of_lists[2]
>>> list_of_lists[2][2][0]
```

### Dictionaries
How would you describe this picture? Confusing? Inspiring? Lmao? Did Anand make this? Why does this make me want to scream?

![Artists](http://i.imgur.com/1lzb3vq.png)

Well, here is how a programmer would describe this picture:
```
>>> artists = ["weeknd", "weeknd", "weeknd", "weeknd", "weeknd", "weeknd", "weeknd", "kendrick", "kendrick", "kendrick", "drake", "drake", "drake", "drake", "kanye"]
```

Copy and paste the above command into your terminal. If you wanted to know how many times Kendrick Lamar appeared in the picture above using one of the list methods we learned above, how would you do it?

But hold on, there is an easier way! This is where dictionaries come in. Dictionaries have *keys* and a *value* for each key. They are actually quite analogous to real dictionaries. If you were to take a dictionary and search for the word "genius", you'd find the definition to be "Kanye West". In this case, "genius" is the *key* you used to find the *value* of "Kanye West".

Now, with this knowledge, this is how that same programmer would describe this picture:
```
>>> artists = {"weeknd": 7, "kendrick": 3, "drake": 4, "kanye": 1}
```

If someone were to ask us how many Kanye Wests there were, it's really easy to find out with a dictionary. We simply type:

```
>>> artists["kanye"]
```

and **BAM**, our dictionary shows us the value of `1` for our key `"kanye"`. I guess there really is just one Kanye.

Go ahead and try the following out to describe yourself in code. You can use some of the same keys as the one below but get creative with your keys and data-types! Write 10 keys for yourself.
```
>>> john = {}
>>> john["eyes"] = "hazel"
>>> john["hair"] = "brown"
>>> john["height"] = 5.8
>>> john["music"] = ["jazz", "hip-hop", "edm"]
>>> john["sports"] = None
>>> john["phone"] = 5551234567
>>> john["skydived"] = False
.
.
.
etc.
```

Now, if John were to type `john` in his Terminal, he'd see his complete dictionary.

Suppose John went skydiving and now wants to change his dictionary. Doing that is easy, all he has to do is type `john["skydived"] = True` and the new value overwrites the old one.

Suppose Jenny gets on his computer and wants to see all the keys John wrote, all she has to do is type `john.keys()`. In this case, it's not a huge deal to see all the keys we write since there are only 10. But often times, as we will see in this course, dictionaries can get **immense** and it's useful to know what categories of data is stored.

Dictionaries are useful when data is associated with a name, like finding someone's *height*, or a car's *make*, *model*, and *license plate*, or the number of *oranges* we have in inventory, etc. and we will be using them extensively in this course.

Congratulations on surviving day one!

![Congrats](https://media.giphy.com/media/FM9nVGQ081zwY/giphy.gif)