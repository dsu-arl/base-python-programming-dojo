# Writing Your Own Module

Since you have become familiar with modules within Python's Standard Library, you now get to learn how to write your own modules that you can reuse in any program you'd like. Writing your own custom modules is helpful for several reasons:

1. They break up your code into multiple files, making your code base easier to understand.
2. They are reusable in any future project.
3. They are tailored to your specific needs, and can easily be edited.

When writing your own python modules, you will need to create two python files. The *first* python file will be your main program, where you are building the bulk of your program. This first file will also be where you `import` your custom module. The *second* file will be the code making up your custom module. These can be as simple, or as complex as you want. 

# Example 

Let's say that you are creating a pirate game. You will want to make a class that represents a pirate, and a pirate has many functions:
- `drink_rum`
- `fight`
- `dig_for_treasure`

You also want to have a ship class. Ship classes can contain many pirates and perform the following functions:
- `hoist_anchor`
- `drop_anchor`
- `moor`
- `set_sail`

Our module file might look something like this:
```python
# game_objects.py
import random

class Pirate:
	def __init__(self):
		self.bac = 0.00
		self.weapon = "sword"
		self.gold_coins = 0

	def drink_rum(self):
		self.bac += random.random()

	def fight(self):
		print(f"The pirate used a {self.weapon} to attack!")

	def dig_for_treasure(self):
		if bool(random.getrandbits(1)):
			self.gold_coins += random.randint(1, 10)

class Ship:
	def __init__(self, name):
		self.pirates = []
		self.name = name
		self.anchored = False
		self.sailing = False

	def hoist_anchor(self):
		self.anchored = False

	def drop_anchor(self):
		self.anchored = True

	def moor(self):
		self.sailing = False

	def set_sail(self):
		self.sailing = True
```

Then, our main game file would look something like this!
```python
# main.py
from game_objects import Pirate, Ship

p = Pirate()
p.drink_rum()
p.fight()
p.dig_for_treasure()

s = Ship(name="S.S. Anselm")
s.pirates.append(p)
s.hoist_anchor()
s.set_sail()
s.moor()
```

Our main game file is less cluttered because the majority of our code is split into a different module file that we then import. *NOTICE* that our import line: `from game_objects import Pirate, Ship` uses the name of the file as the module name, and then each class is specified. You could also do `import game_objects`, but then you would have to create objects like this: `p = game_objects.Pirate()` & `s = game_objects.Ship(name="S.S. Anselm")`

For this challenge:
1. Create a python module file named `my_module.py`.
	- Create a Dog class with 2 functions: `sit` and `bark`. These functions can just print out "sit" and "bark!" respectively. 
	- Create a Cat class with 2 functions: `knock_stuff_over` and `meow`. These functions can print out "The cat knocked over a \_\_\_\_\_." (you choose) and "meow!" respectively. 
2. Create a main file called `main.py`. 
	- Import the code from your module any way you want.
	- Create one instance of the Cat class and one of the Dog class.
	- Call both of the functions that each has. 

Run `/challenge/verify <your_python_main_file> <your_python_module_file>` to get your flag!
