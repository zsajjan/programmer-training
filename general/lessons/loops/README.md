# LOOPS

#### making code repeat over and over

**Loops** allow you to repeat the same code more than once without just writing it a bunch of times.
* For-loop: iterate (go over each of) several values, running the same code again and again on each new value
* While-loop: repeat code as long as some condition is true

### Example of a _while_ loop:

    while raw_input() == “again!”:
        print “Wheeee!”

output of this program:

    again!
    Wheeee!
    again!
    Wheeee!
    done

### Example of a _for_ loop:

    for i in range(0, 10):
  	    print i * i

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

While loops are sort of like `if` statements, except that when it's done, it tests the condition again and repeats if it evaluates to `true`. `for` loops iterate through a list (the next lesson is about lists) of variables, but for now just use the `range()` function to create a list. Notice that in the example above, `range(0, 10)` creates a list of all integers greater than or equal to 0 (the first parameter) and less than (but not equal to) 10 (the second parameter). It's a common practice to use `i` for the iterator variable in a `for` loop, and if loops are nested, the inner one will be `j`, `k`, and so on (alphabetical order).

##### DO NOT HAVE TOO MANY LOOPS INSIDE EACH OTHER

If you do, it will quickly get **very** confusing and hard to follow.
