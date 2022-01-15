Toolium Template
================

Base project to start using `Toolium <https://github.com/Telefonica/toolium>`_ for your testing automation projects
(web, Android or iOS).

The toolium-template example test is a behave web test. There are more examples of web, Android or iOS tests (with or
without using behave) in `toolium-examples <https://github.com/Telefonica/toolium-examples>`_.

Getting Started
---------------

Clone `toolium-template <https://github.com/Telefonica/toolium-template>`_ repository and install requirements. It's
highly recommendable to use a virtualenv.

.. code:: console

    $ git clone https://github.com/Telefonica/toolium-template.git
    $ cd toolium-template
    $ pip install -r requirements.txt

Running Tests
-------------

By default, example tests are configured to run in chrome locally, so chrome must be installed in your machine and the
chrome driver must be downloaded and configured:

- Download `chromedriver_*.zip <http://chromedriver.storage.googleapis.com/index.html>`_
- Unzip file and save the executable in a local folder
- Configure driver path in *[Driver]* section in `conf/properties.cfg` file ::

    [Driver]
    chrome_driver_path: C:\Drivers\chromedriver.exe

To run all tests:

.. code:: console

    $ behave

To run a single test:

.. code:: console

    $ behave -n 'successful login'

Customizing Template
--------------------

Before creating your tests, you should personalize the template:

1. Clone toolium-template repository

.. code:: console

    $ git clone git@github.com:Telefonica/toolium-template.git <your_repository_name>

2. Compact all template commits in one preserving the author

.. code:: console

    $ cd <your_repository_name>
    $ git reset $(git commit-tree HEAD^{tree} -m "Toolium template")
    $ git -c user.name="Ruben Gonzalez Alonso" -c user.email=rgonalo@gmail.com commit --amend --reset-author --no-edit

3. Create a new clean repository in your github user/organization

4. Replace origin and push changes yo your repository

.. code:: console

    $ git remote rm origin
    $ git remote add origin git@github.com:<your_github_organization_or_user>/<your_repository_name>.git
    $ git push -u origin master
