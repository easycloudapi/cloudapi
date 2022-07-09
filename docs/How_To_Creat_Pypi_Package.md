## How to create package and deploy to PyPi

#### Ref: https://towardsdatascience.com/how-to-publish-a-python-package-to-pypi-7be9dd5d6dcd
#### Ref: https://packaging.python.org/en/latest/tutorials/packaging-projects/

1. create virtual-env: 
	```bash
	python -m venv env --system-site-packages
	```
2. activate the virtual env:
	* windows: 
		```bash
		env\Scripts\activate
		```
	* unix: 
		```bash
		source env/bin/activate
		```
3. upgrade pip: 
	```bash
	pip install --upgrade pip
	```
4. install setuptools and wheel: 
	```bash
	python -m pip install setuptools wheel
	```
5. run the setup.py to create the package:
	```bash
	python setup.py sdist bdist_wheel
	```
6. locally install the package for testing (run from root dir where setup.py available): 
	```bash
	pip install -e .
	pip uninstall cloud_utility
	```
7. create account on testpypi: 
	Navigate to https://test.pypi.org/ and register
8. install twine which will copy the code to pypi:
	```bash
	python -m pip install twine
	```
9. copy the package to testpypi:
	```bash
	python -m twine upload --repository testpypi dist/*
 	python -m twine upload --skip-existing --repository testpypi dist/*
	```
10. install from testpypi locally: 
	```bash
	pip install -i https://test.pypi.org/simple/ cloud-utility==0.0.1
	```
11. create account on pypi:
11. copy the package to pypi:
	```bash
	python -m twine upload dist/*
	```
12. from next release, copy the package to pypi:
	```bash
 	python -m twine upload dist/* --verbose
	python -m twine upload --skip-existing dist/*
 	```
