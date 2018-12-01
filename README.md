SKA Skeleton Project
====================

Briefly describe your project here

Install 
-------

**Always** use a virtual environment. [Pipenv](https://pipenv.readthedocs.io/en/latest/) is now Python's officially
recommended method and the one used by default in this repo.

Follow these steps at the project root:

```bash
pip install pipenv # if you don't have pipenv already installed on your system
pipenv install
pipenv shell
```

You will now be inside a pipenv shell with your virtual environment ready.

Use `exit` to exit the pipenv environment.


Testing
-------

* Put tests into the `tests` folder
* Use [PyTest](https://pytest.org) as the testing framework
  - Reference: [PyTest introduction](http://pythontesting.net/framework/pytest/pytest-introduction/)
* Run tests with `python setup.py test`
  - Configure PyTest in `setup.py` and `setup.cfg`
* Running the test creates the `htmlcov` folder
    - Inside this folder a rundown of the issues found will be accessible using the `index.html` file
* All the tests should pass before merging the code 
 
 Code analysis
 -------------
 * Use [Pylint](https://www.pylint.org) as the code analysis framework
 * By default it uses the [PEP8 style guide](https://www.python.org/dev/peps/pep-0008/)
 * Use the provided `code-analysis.sh` script in order to run the code analysis in the `module` and `tests`
 * Code analysis should only raise document related warnings (i.e. `#FIXME` comments) before merging the code
 
Writing documentation
 --------------------
 * The documentation generator for this project is derived from SKA's [SKA Developer Portal repository](https://github.com/ska-telescope/developer.skatelescope.org)
 * The documentation can be edited under `./docs/src`
 * In order to build the documentation for this specific project, execute the following under `./docs`:
 ```bash
make html
```
* The documentation can then be consulted by opening the file `./docs/build/html/index.html`
