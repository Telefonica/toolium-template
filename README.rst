Toolium Template
================

Base project to start using `Toolium <https://github.com/Telefonica/toolium>`_ for your testing automation projects
(web, Android or iOS).

Getting Started
---------------

The requirements to install Toolium are `Python 2.7 or 3.3+ <http://www.python.org>`_ and
`pip <https://pypi.python.org/pypi/pip>`_. If you use Python 2.7.9+, you don't need to install pip separately.

Clone `toolium-template <https://github.com/Telefonica/toolium-template>`_ repository and install requirements. It's
highly recommendable to use a virtualenv.

.. code:: console

    $ git clone git@github.com:Telefonica/toolium-template.git
    $ pip install -r requirements.txt

Running Tests
-------------

By default, example tests are configured to run in firefox locally, so firefox must be installed in your machine.

To run all tests:

.. code:: console

    $ nosetests tests

To run a single test:

.. code:: console

    $ nosetests tests/test_login.py:Login.test_successful_login_logout
