A Python library for implementing Tin Can API.

For hosted API documentation, basic usage instructions, supported version listing, etc. visit the main project website at:

<http://rusticisoftware.github.io/TinCanPython/>

For more information about the Tin Can API visit:

<http://tincanapi.com/>

Requires Python 2.7 or later.

## Installation
TinCanPython requires [Python 2.7](https://www.python.org/downloads/) or later. Python 3 is not supported.

If you are installing from the Github repo, you will need to install `aniso8601` and `pytz` (use `sudo` as necessary):

    easy_install aniso8601 pytz

### Recommended optimization
To speed up the timezone lookups, run:

    pip unzip pytz

## Testing
The preferred way to run the tests is from the command line.

### Unix-like systems and Mac OS X
No preparation needed.

### Windows
Make sure that your Python installation allows you to run `python` from the command line. If not:

1. Run the Python installer again.
2. Choose "Change Python" from the list.
3. Include "Add python.exe to Path" in the install options. I.e. install everything.
4. Click "Next," then "Finish."

### Running the tests
It is possible to run all the tests in one go, or just run one part of the tests to verify a single part of TinCanPython. The tests are located in `test/`.

#### All the tests:
1. `cd` to the `test` directory.
2. Run

        python main.py

#### One of the tests:
1. `cd` to the directory containing the test.
2. Run

        python result_test.py

    (or whatever test you want to run)

#### A single test case of one of the tests:
1. `cd` to the directory containing the test.
2. Run

        python -m unittest remote_lrs_test.RemoteLRSTest.test_retrieve_statement

    Where "remote_lrs_test" is the test file, "RemoteLRSTest" is the class in that file, and "test_retrieve_statement" is the specific test case.

## API doc generation
To automatically generate documentation, at the root of the repository run,

    sphinx-apidoc -o ./docs/source/ tincan/

Then from the `docs/` directory run,

    make html

The docs will be output to `docs/build/html/`.

If you would like to change the names of each section, you can do so by modifying `docs/source/tincan.rst`.

## Releasing