# my_first_python_lib

See https://medium.com/analytics-vidhya/how-to-create-a-python-library-7d5aea80cc3f 

My example how to create a Python library.


## Build the library

```shell
pip install --upgrade pip setuptools wheel twine
```

```shell
python setup.py pytest
```


```shell
python setup.py bdist_wheel
```
A wheel file will be created in the `dist` folder.
The library can be installed using `pip`. 
```shell
pip install dist/mypythonlib-0.1.0-py3-none-any.whl
```

```python
import mypythonlib
from mypythonlib import myfunctions
```