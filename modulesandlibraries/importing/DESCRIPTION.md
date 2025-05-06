# Importing Modules or Libraries

In order for us to use code that is found in modules and libraries, we first need to tell our code to include it. We do this through the Python keyword `import`. `import` statements ought to be put at the top of your Python file so that when you run your code, the modules and libraries get imported first before you attempt to use them.

Let's see an example of importing the `socket` library:
```python
import socket

my_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)

```

In the above code you can see that I first imported the `socket` library, and then I used it to create a socket called `my_socket`.

Start the challenge and run `/challenge/verify` to get further instructions!
You will be using the `math` module, you can find helpful information [here](https://docs.python.org/3/library/math.html) to aid you!
