# LOOPS

#### making code repeat over and over

**Loops** allow you to repeat the same code more than once without just writing it a bunch of times.
* **`For` loop:** iterate (go over each of) several values, running the same code again and again on each new value
* **`While` loop:** repeat code as long as some condition is true

### Example of a _while_ loop:

```
while raw_input() == “again!”:
    print “Wheeee!”
```

output of this program:

    again!
    Wheeee!
    again!
    Wheeee!
    done

### Example of a _for_ loop:

```
for i in range(0, 10):
    print i * i
```

output of this program:

    0
    1
    4
    9
    16
    25
    36
    49
    64
    81

## More about loops

While loops are sort of like `if` statements, except that when it's done, it tests the condition again and repeats if it evaluates to `True`. `for` loops create a variable (in this example, `i`) that iterates through a list of variables. In many cases, you'll want to use the `range()` function to create a list. Notice that in the example above, `range(0, 10)` creates a list of all integers greater than or equal to 0 (the first parameter) and less than (but not equal to) 10 (the second parameter). It's a common practice to use `i` for the iterator variable in a `for` loop, and if loops are nested, the inner ones will be `j`, `k`, and so on (alphabetical order).

### DO NOT HAVE TOO MANY LOOPS INSIDE EACH OTHER

If you do, it will quickly get **very** confusing and hard to follow. In most cases, 'too many' is about 3 to 5.

### DO NOT CREATE CODE THAT REPEATS FOREVER

In terminal, try running `cat /dev/urandom` or `yes This is an infinite loop`. Not very fun, is it? Here's a python program that does the same thing:

```
while (True):
    print "Infinite loops are evil."
```
