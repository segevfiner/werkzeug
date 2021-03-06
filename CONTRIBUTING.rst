=============================
How to contribute to Werkzeug
=============================

Thanks for considering contributing to Werkzeug.

Support questions
=================

Please, don't use the issue tracker for this. Check whether the `Pocoo IRC
channel <http://www.pocoo.org/irc/>`_ can help with your issue. If your problem
is not strictly Werkzeug- or Flask-specific, ``#python`` on Freenode is
generally more active.  `StackOverflow <https://stackoverflow.com/>`_ is also
worth considering.

Reporting issues
================

- Under which versions of Python does this happen? This is even more important
  if your issue is encoding related.

- Under which versions of Werkzeug does this happen? Check if this issue is
  fixed in the repository.

Submitting patches
==================

- Please do not use pull requests as a way to suggest behavior changes. Open an
  issue for discussion first. This helps keeping the discussions of concept and
  implementation separate.

- Include tests if your patch is supposed to solve a bug, and explain
  clearly under which circumstances the bug happens. Make sure the test fails
  without your patch.

- Try to follow `PEP8 <http://legacy.python.org/dev/peps/pep-0008/>`_, but you
  may ignore the line-length-limit if following it would make the code uglier.

- Add an entry to ``CHANGES`` and your name to ``AUTHORS``.


Running the testsuite
---------------------

Set up a `virtualenv
<https://virtualenv.readthedocs.io/en/latest/index.html>`_::

    python3 -m venv venv
    . venv/bin/activate

Install Werkzeug in editable mode::

    pip install -e .

Install the minimal test requirements::

    pip install pytest requests

Then you can run the testsuite with::

    pytest

With only ``pytest`` installed, a large part of the testsuite will get skipped
though.  Whether this is relevant depends on which part of Werkzeug you're
working on.  Travis is set up to run the full testsuite when you submit your
pull request anyways.

If you really want to test everything, you will have to install ``tox``::

    pip install tox

The ``tox`` command will then run all tests against multiple combinations
Python versions and dependency versions.
