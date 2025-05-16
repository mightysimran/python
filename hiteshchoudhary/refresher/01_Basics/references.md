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