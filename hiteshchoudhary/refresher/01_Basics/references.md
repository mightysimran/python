# Inner Working Of Python

**init.py → bytecode (mostly hidden) → Python Virtual Machine**

1. Compile to bytecode (low level and platform independent)
2. bytecode runs faster | .pyc - compiled python (frozen binaries)
3. **\_\_pycache\_\_** folder | Source Change and Python Version
4. \_\_pycache\_\_ is ***only*** created when importing files, whether nested inside subdirectories or at root.


**Python Virtual Machine**
- fetches and executes bytecode instructions — iterates.
- Run-time engine.
- Known as ***Python Interpreter***

**Important** -> bytecode is not Machine Code
- python specific interpretation
- cpython (standard implementation), jython, iron python, stackless, pypy

# Python Shell (REPL)

python is **computational**.

Here's how you can work with python shell:
- IDLE (Python 3.x 64-bit)
- Terminal (win) → **python** 
- Terminal (mac/linux) → **python3**

To exit the Python shell (REPL) from the terminal, press `Ctrl+D` or `Ctrl+Z` followed by `Enter`.

```
>>> print("Hello, world.")
Hello, world.

>>> for char in "python":
...     print(char)
...     
p
y
t
h
o
n

>>> import sys
>>> sys.platform
'win32'

>>> import HelloWorld
Hello, world.
>>> HelloWorld.hi("traveler")
Hello, traveler

>>> HelloWorld.lang
Traceback (most recent call last):
  File "<python-input-1>", line 1, in <module>
    HelloWorld.lang
AttributeError: module 'HelloWorld' has no attribute 'lang'

>>> from importlib import reload
>>> reload(HelloWorld)
Hello, world.
<module 'HelloWorld' from '/Users/mightysimran/Documents/python/hiteshchoudhary/refresher/01_Basics/HelloWorld.py'>

>>> HelloWorld.lang
'python'
```

# Data types (or object types) 

- **Number**: 1024, 3.14, 5+4j, 0b111, Decimal(), Fraction()
- **String**: 'python', "mightysimran's", b'a\x01c', u'na\xf1o'
- **List** : [1, [25, 'python'], 4.54], list(range(10))
- **Tuple** : (1, 'nano', 4, 'x'), tuple('nano'), namedtuple
- **Dictionary** : {'name': 'mightysimran', 'lang': 'python'}, dict(hours=4)
- **Set** : set('abc'), {'a', 'b', 'c'}
- **File** : open('notes.txt', 'w), open(r'C:\notes.bin', 'wb')
- **Boolean** : True, False
- **None** : None
- functions, modules, classes
- adv - Decorators, Generators, Iterators, MetaProgramming

```
>>> import math
>>> math.pi
3.141592653589793

>>> import random
>>> random.random()
0.08353950308467084

>>> random.choice([1,2,3,4,5])
4

>>> s="extraordinary"
>>> len(s)
13

>>> name[0]
'e'

>>> name[-1]
'y'

>>> name[-2]
'r'

>>> name[1:4]
'xtr'

>>> dir(name)
['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__getstate__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isascii', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'removeprefix', 'removesuffix', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']

>>> l = [1,2,3]
>>> l.append(4)
>>> l[0] = -1
>>> del l[2]

>>> t = (1, 2, 3) # modifs not allowed

>>> d = {'x': 1}
>>> d['y'] = 4
>>> del d['y']
```