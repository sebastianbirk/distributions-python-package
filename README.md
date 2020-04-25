# Python Package: Distributions
This repository contains my (statistical) distributions python package which has APIs to easily work with Gaussian and Binomial distributions.

More importantly than that, the repository can be used as a tutorial/blueprint for building a new Python package using pip and uploading it to PyPi.

## Contents

| File/folder                             | Description                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------|
| `distributions`                         | Contains the code for the distributions package including                                                                               Generaldistribution.py, Gaussiandistribution.py and Binomialdistribution.py                                                             as well as the \_\_init\_\_.py file which is ran when the                                                                               package is imported.                                                        |
| `setup.py`                              | A file needed for building Python packages with pip.                        |
| `test.py`                               | Unit tests to help debug code.                                              |
| `numbers.txt`, `numbers_binomial.txt`   | Data files used as part of the unit tests.                                  |

## Instructions

To install the distributions package using pip, clone this repository, navigate to the folder that contains the repository source files and then run

```
pip install .
```

If you have already installed the package but need to make changes and then update the package, run

```
pip install --upgrade .
```

To run the unit tests type

```
python -m unittest test
```
