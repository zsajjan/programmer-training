## Python Interpreter
* So far, all of the code you’ve written has been in the Python interpreter
* The interpreter is great for testing ideas or simple one-liners
* It does not easily allow you to save your code between runs
* If you want to work on a program where you will be frequently editing, saving and working on your code, the interpreter is not ideal

## Vim
* Take a look at the [lesson on vim](/general/lessons/vim).
* Once you've installed vim, you can type `vim <filename` into terminal to open that file. If the file doesn't exist, it creates a new file.
* Before typing anything, press `i` to go into insert mode (so you can actually type). You can then press `Esc` to go into normal mode. Then you can type `:w` to write (save) a file and `:q` to quit (close a file).
* Make sure you use the `.py` extension on all your python files. Otherwise, you won't get nice color coding. That would be sad.

## Running a python program
* Use `cd` and `ls` to navigate to the directory your file is in.
* Type `python <name of your program>.py`. Press `enter`. Observe the following demo:


``

    cd ~/robotics/training
    $ ls
    test.py
    $ python test.py
    test: It works!
    It works!

Try printing these arithmetic calculations and see what happens!

    5 + 9
    4 * 2 - 3
    7 * 10 ** .5

Once you are familiar with these, try one that shows 5 arithmetic expressions of your choice that results in the number 42. Feel free to look up how to do any fancy expressions.

## Order of operations
Arithmetic calculations in python follow the order of operations. Here is the hierarchy (PEMDAS): 

* `()` **P**arentheses  
* `**` **E**xponent
* `*` **M**ultiplication
* `/` **D**ivision
* `+` **A**ddition
* `-` **S**ubtraction

When you divide two numbers without decimals, the result is always rounded down. For example:

    5 / 2 = 2

When at least one of the numbers you’re dividing is a decimal number, python interprets this as regular division and gives correct results:

    5.0 / 2 = 2.5
    5.0 / 2.0 = 2.5

We’ll talk more about this phenomenon later!

## Try it!
Print arithmetic expressions in both the python interpreter and by running files.
