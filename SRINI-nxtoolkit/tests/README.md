Toolkit Unit Tests
==================

The nxtoolkit package has a unit test suite that strives for a
minimum of 100% code coverage.  The main test suite is contained
within the ``nxtoolkit_test.py`` file.  Within the test suite, the
tests can be classified into 2 types; live tests and offline tests.
Live tests are those that actually communicate with a switch and push
configuration to/from the Switch.  Offline tests run locally and do not
communicate with the Switch in any way.

The tests are can be run in the following ways::

    python nxtoolkit_test.py [offline | live | full ]

The optional keyword allows ``offline``, ``live``, or the ``full``
testsuite to be run. If the keyword is not provided, the default of
``offline`` will be used.

When adding additional code or making changes to the toolkit, please
ensure that unit tests are added to cover the new functionality and
that the entire test suite is run against the modified toolkit before
submitting the code.  Minimal code coverage can be verified using
tools such as
[coverage.py](https://pypi.python.org/pypi/coverage). For instance,
after installing coverage.py, the toolkit can be run with the
command::

    coverage run nxtoolkit_test.py

and an HTML report of the code coverage can be generated with the
command::

    coverage html

If changes are made to the ``nxtoolkit.py`` file, please ensure that
the ``nxtoolkit_test.py`` is run and that code coverage remains at
100%.

