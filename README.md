# my_first_python_lib

A example how to create a Python library.

For more details see https://packaging.python.org/en/latest/tutorials/packaging-projects/

## Build the Package
Requirements to create a package and upload it.
```shell
pip install - -upgrade pip  setuptools wheel twine
```
Its good practice to test everything. 
```shell
python setup.py pytest
```
Create a wheel file in the `dist` folder.
```shell
python setup.py sdist bdist_wheel
```
The local package can also be installed using `pip`.

```shell
pip install dist/*.whl
```

## Publish the Package

1. Head to https://pypi.org/ and create an account. 
2. Make sure the `setup.py` name is not used and the account information match.
3. Upload the package
```shell
twine upload dist/*
```

## Use the Package
I haven't actually uploaded it.
```shell
pip install mypythonlib
```
```python
from mypythonlib import myfunctions

myfunctions.haversine(4.895168, 52.370216, 13.404954, 52.520008) 
```

