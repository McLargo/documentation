## PEP 8

- use 4 spaces, instad of tab
- use two line breack to separate class or methods
- use one line breack between methods inside a class
- how to import library
	- standard libraries
    - 3pp libraries
	- django libraries
	- local importation

    **CAREFUL while doing import**

    - it is relative import if it is same app: _.{class}_
    - better use absolute import: _{app}.{class}_
    - avoid using _from something import *_

- use `_` instead of `-`
- avoid use of abbreviature while defining variable, classes or methods
- one empty line at the end of the file
- 79 max length of line
- use flake8 and [pylint](https://github.com/PyCQA/pylint/blob/master/pylintrc), standard libraries to check pep8 and lintº