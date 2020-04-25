# Python Package: Distributions
This repository contains my (statistical) distributions python package which has APIs to easily work with Gaussian and Binomial distributions.

More importantly than that, the repository can be used as a tutorial/blueprint for building a new Python package using pip and uploading it to PyPi (Python Package Index).

## Contents

| File/folder                             | Description                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------|
| `distributions`                         | Contains the code for the distributions package including                                                                               Generaldistribution.py, Gaussiandistribution.py and Binomialdistribution.py                                                             as well as the \_\_init\_\_.py file which is ran when the                                                                               package is imported.                                                        |
| `setup.py`                              | A file needed for building Python packages with pip.                        |
| `test.py`                               | Unit tests to help debug code.                                              |
| `numbers.txt`, `numbers_binomial.txt`   | Data files used as part of the unit tests.                                  |

## Instructions

### Install the package using pip

To install the distributions package using pip, clone this repository, navigate to the folder that contains the repository source files and then run

```
pip install .
```

Take a look at the setup.py file which is used by pip if you want to create a new package.

If you have already installed a package but need to make changes and then update the package, run

```
pip install --upgrade .
```

### Run and build unit tests

To run the unit tests type

```
python -m unittest test
```

Take a look at the test.py file which contains some example unit tests if you want to create a new package.

### Upload the package to PyPi (https://pypi.org/, https://test.pypi.org/)

When you run ```pip install [package-name]``` you are downloading and installing files from PiPy. Anyone can upload files to PiPy. PiPy has a test as well as a regular repository. First upload your package to the rest repository to make sure the download works as expected, then you can upload the package to the regular repository. If the package is in the regular repository, anyone can download it.

To upload files to PyPi, you first need to create accounts for the pypi test repository and pypi regular repository. Note that pypi.org and test.pypy.org are two different websites. You'll need to register separately at each website. 

You also need some additional files in your source code:
- README.md
- license.txt
- setup.cfg

See the source files in this repository for details what they should contain.

Then enter your terminal, go to your source code and enter the following commands:

```
python setup.py sdist
pip install twine
```

- Uploading to the PyPi test repository and installing from there:
```
twine upload --repository-url https://test.pypi.org/legacy/ dist/*
pip install --index-url https://test.pypi.org/simple/ stats_distributions_utils
```

- Uploading to the PyPi regular repository and installing from there:
```
twine upload dist/*
pip install stats_distributions_utils
```


