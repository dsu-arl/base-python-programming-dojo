# Different Ways to Import Modules

In this challenge, you will learn two different ways we can import modules.

# `import as`

The first method uses the `import as` syntax. Sometimes, a modules name is really long, and we don't want to have to type it over and over again when we use it in our code. To get around that, we can give this new module an `alias`. The following two examples demonstrates thise.

```python
import socket

my_sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
```

```python
import socket as s

my_sock = s.socket(socket.AF_INET, socket.SOCK_STREAM)
```

You can see that in the second example, I use the `import as` syntax. `import socket as s` allows us to use the socket module under the alias `s`. So now we don't have to type out the full module name when we are using it.

# `from import`

The second method uses the `from import` syntax. When you import a module like in our last challenge (`import math`). It imports ALL the functions within that file. If you only need one function from the math module, this means that there are a lot of functions that are imported into your program that you aren't using, which can slow your run time. Thankfully, python gives us the ability to import only what we need!

```python
import math

number = math.sqrt(4)
```

```python
from math import sqrt
number = sqrt(4)
```

In the examples provided, you can see the difference in how we are importing our math function. In the first one, we include ALL of the math module. This is typically fine for smaller programs, but in larger applications, you don't want unnecessary dead weight. In the second example, you can see that we import ONLY the `sqrt` function `from` the `math` module. This keeps our program lightweight while giving us the desired functionality we need. 

For this challenge you need to:
1. Create one python file.
2. Import the `floor` function from the `math` module.
	- Use the `floor` function on a decimal number, and print out it's result.
3. Import the `argparse` module, but alias it as `ap`.
	- You don't need to use this module.
4. Run `/challenge/verify <yourpythonfile>` to get the flag.
