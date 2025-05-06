# Modules and Libraries

One of Python's strength as a programming language has to do with the fact that it has MANY built in modules and libraries (referred to as Python's Standard Library). On a very basic level `Modules` and `Libraries` are specific pieces of code that we can include into our own code. These modules and libraries can extend the functionality of our code, and allow us to do a lot more with the Python programming language. The difference between a module and a library is that a module is a single Python file, whereas a library is made up of multiple Python files that tie together. However, functionally, using a module and library function the same on our end.

As an example, there is a `module` called `math` in the Python standard library. If you `import` the `math` module into your code, it allows you to perform more complex calculations that are normally not as simple in the base Python language.

Here is an example of trying to find the square root of a given number without the `math` library.
```python
num = 144

def get_square_root(number):
    if number < 0:
        return -1   # Returning a -1 will signifiy the function failed.

    if number == 0:
        return 0

    # Iterate through and find square root
    for i in range(1, number // 2):
        if i * i == number:
            return i

    return -1

x = get_square_root(num)
print(x) # will print 12
```

Here is an example of trying to find the square root of a given number with the `math` library.
```python
import math

num = 144
x = math.sqrt(num)
print(x)    # will print 12.0
```
Do you see how much easier that is? Someone else has gone through the work of programming the square root function for us, so let's not reinvent the wheel!

In this module, you will learn how to utilize modules and libraries within Python's standard library. All of the modules and libraries in Python's standard library come pre-packaged with Python, so you won't need to install anything extra. There are millions of modlues and libraries created by people on the internet that you can download and use in your own code, but we will look at those later.

You can browse [here](https://docs.python.org/3/library/index.html) to look through a list of Python's Standard Library and see what it has to offer!
