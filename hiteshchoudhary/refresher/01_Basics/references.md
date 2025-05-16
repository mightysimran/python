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
