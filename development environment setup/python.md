## Python pip / pip3

- Python2 and Python3 are incompatible

- pip is for python2 , pip3 is for python3

```shell
    # show pip /pip3 verison
      ting@ting-desktop:~$ pip --version
      pip 20.3.4 from /usr/local/lib/python2.7/dist-packages/pip (python 2.7)

      ting@ting2-desktop:~$ pip3 --version
      pip 21.2.4 from /home/ting/.local/lib/python3.6/site-packages/pip (python 3.6)

    # upgrade pip /pip3
      python -m pip install --upgrade pip    or    pip install --upgrade pip
      python3 -m pip install --upgrade pip   or    pip3 install --upgrade pip

    # list package
      pip list      /    pip show *packagename*
      pip3 list     /    pip3 show *packagename*
```

- [PyPI · The Python Package Index](https://pypi.org/)



</br>

## Python virtual enviroment

[**Anaconda**](https://www.anaconda.com/) is the better choice but it's large so it is not suitable for Nano. The Nano sdcard ROM size is small, depending on the size of sdcard used, 32G, 64G or 128G and even larger.

So use [virtualenv](https://pypi.org/project/virtualenv/) or [python3-venv](https://docs.python.org/3/tutorial/venv.html) in Nano


⚠️ ~~pyenv~~ was deprecated ≧ Python3.6

⭐ In teh virtual env, **should not** use `sudo pip/pip3 install ...` , it will install the package into the global environment ; </br>
&emsp;&nbsp;&nbsp;should use `pip/pip3 install ...` to install package correctly in the target virtual env instaed.

```shell

# install virtualenv
  pip3 install virtualenv

  pip3 list | grep -i virtualenv

  python3 -m virtualenv --help

# create virtualenv
  virtualenv -p */usr/local/bin/python3* *venv name*
      # -p python version, optional
      # Should not use '--system-site-packages', it'll impact the global env when upgrade the existing packge.

# activate
  source *venv_path/bin/activate

# deactivate
  (venv) deactivate
```


⚠️ Onec the *venv* was created, can't rename, move or copy it.</br>
&emsp;&nbsp;&nbsp;Should use the another package like virtualenv-clone or else to clone venv,</br>
&emsp;&nbsp;&nbsp;or use 'requirement.txt' to export/import the venv.

_< trick >_&ensp;For clone pacakge between the diffrence venv with the same python version and which pacakge dependencies,</br>
&emsp;&emsp;&emsp;&emsp;&nbsp;can copy packages under 'dist-packages' or 'site-package' to the new target venv directly.

</br>

## Python common

- [Python requirements.txt](https://www.google.com/search?q=python+requirements.txt&rlz=1C1GCEU_zh-TWTW892TW892&oq=python+requirement&aqs=chrome.0.0i512j69i57j0i512l8.7609j0j15&sourceid=chrome&ie=UTF-8)

```shell
    # export package requirements
      pip freeze > requirements.txt

    # import package requirements
      pip install -r requirements.txt
```

- [Python Juypter Notebook](https://jupyter.org/)


</br>

## Python basics

```shell
    python -c "command"

    python -m "Module" # Module is a *.py. Contains all variables and functions within it.

    >>> dir(__builtins__) # Query built-in functions
    ['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException', 'BlockingIOError', 'BrokenPipeError', 'BufferError', 'BytesWarning', 'ChildProcessError', 'ConnectionAbortedError', 'ConnectionError', 'ConnectionRefusedError', 'ConnectionResetError', 'DeprecationWarning', 'EOFError', 'Ellipsis', 'EnvironmentError', 'Exception', 'False', 'FileExistsError', 'FileNotFoundError', 'FloatingPointError', 'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning', 'IndentationError', 'IndexError', 'InterruptedError', 'IsADirectoryError', 'KeyError', 'KeyboardInterrupt', 'LookupError', 'MemoryError', 'ModuleNotFoundError', 'NameError', 'None', 'NotADirectoryError', 'NotImplemented', 'NotImplementedError', 'OSError', 'OverflowError', 'PendingDeprecationWarning', 'PermissionError', 'ProcessLookupError', 'RecursionError', 'ReferenceError', 'ResourceWarning', 'RuntimeError', 'RuntimeWarning', 'StopAsyncIteration', 'StopIteration', 'SyntaxError', 'SyntaxWarning', 'SystemError', 'SystemExit', 'TabError', 'TimeoutError', 'True', 'TypeError', 'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError', 'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning', 'ValueError', 'Warning', 'ZeroDivisionError', '__build_class__', '__debug__', '__doc__', '__import__', '__loader__', '__name__', '__package__', '__spec__', 'abs', 'all', 'any', 'ascii', 'bin', 'bool', 'bytearray', 'bytes', 'callable', 'chr', 'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr', 'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter', 'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash', 'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter', 'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min', 'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit', 'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted', 'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']

    >>> len(dir(__builtins__))
    152

    help() # function usage

    type()

    isinstance()

    issubclass()

    is()

    id() # object unique ID
```

</br>

⭐ The path of python should use **/** the same as Linux/Brower.


