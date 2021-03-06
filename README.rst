.. You should enable this project on travis-ci.org and coveralls.io to make
   these badges work. The necessary Travis and Coverage config files have been
   generated for you.

.. image:: https://travis-ci.org/terriajs/ckanext-terria_view.svg?branch=master
    :target: https://travis-ci.org/terriajs/ckanext-terria_view

.. image:: https://coveralls.io/repos/terriajs/ckanext-terria_view/badge.svg
  :target: https://coveralls.io/r/terriajs/ckanext-terria_view

.. image:: https://pypip.in/download/ckanext-terria_view/badge.svg
    :target: https://pypi.python.org/pypi//ckanext-terria_view/
    :alt: Downloads

.. image:: https://pypip.in/version/ckanext-terria_view/badge.svg
    :target: https://pypi.python.org/pypi/ckanext-terria_view/
    :alt: Latest Version

.. image:: https://pypip.in/py_versions/ckanext-terria_view/badge.svg
    :target: https://pypi.python.org/pypi/ckanext-terria_view/
    :alt: Supported Python versions

.. image:: https://pypip.in/status/ckanext-terria_view/badge.svg
    :target: https://pypi.python.org/pypi/ckanext-terria_view/
    :alt: Development Status

.. image:: https://pypip.in/license/ckanext-terria_view/badge.svg
    :target: https://pypi.python.org/pypi/ckanext-terria_view/
    :alt: License

=============
ckanext-terria_view
=============

Preview CKAN data on an instance of TerriaJS. Adds itself automatically
to supported resources. Also able to configure as custom views.

------------
Requirements
------------

Built with CKAN 2.7.

------------
Installation
------------

.. Add any additional install steps to the list below.
   For example installing any non-Python dependencies or adding any required
   config settings.

To install ckanext-terria_view:

1. Activate your CKAN virtual environment, for example::

     . /usr/lib/ckan/default/bin/activate

2. Install the ckanext-terria_view Python package into your virtual environment::

     pip install ckanext-terria_view

3. Add ``terria_view`` to the ``ckan.plugins`` 
   settings in your CKAN config file (by default the config file is located at
   ``/etc/ckan/default/production.ini``).

4. Restart CKAN. For example if you've deployed CKAN with Apache on Ubuntu::

     sudo service apache2 reload


---------------
Config Settings
---------------

Document any optional config settings here. For example::

    # Default Instance Title (optional, default: National Map).
    ckanext.terria_view.default_title = National Map
    
    # Default Instance Url (optional, default: //nationalmap.gov.au).
    # Use protocol independent url to not encounter security issues
    ckanext.terria_view.default_instance_url = //nationalmap.gov.au

Enable CORS in ckan unless instance is on the same origin.

Can also add ``terria_view`` to ``ckan.views.default_views`` if you want this
view to be added to all new resources of supported formats.

------------------------
Development Installation
------------------------

To install ckanext-terria_view for development, activate your CKAN virtualenv and
do::

    git clone https://github.com/terriajs/ckanext-terria_view.git
    cd ckanext-terria_view
    python setup.py develop
    pip install -r dev-requirements.txt


-----------------
Running the Tests
-----------------

To run the tests, do::

    nosetests --nologcapture --with-pylons=test.ini

To run the tests and produce a coverage report, first make sure you have
coverage installed in your virtualenv (``pip install coverage``) then run::

    nosetests --nologcapture --with-pylons=test.ini --with-coverage --cover-package=ckanext.terria_view --cover-inclusive --cover-erase --cover-tests


---------------------------------
Registering ckanext-terria_view on PyPI
---------------------------------

TODO: this does not work in ubuntu any more

ckanext-terria_view should be availabe on PyPI as
https://pypi.python.org/pypi/ckanext-terria_view. If that link doesn't work, then
you can register the project on PyPI for the first time by following these
steps:

1. Create a source distribution of the project::

     python setup.py sdist

2. Register the project::

     python setup.py register

3. Upload the source distribution to PyPI::

     python setup.py sdist upload

4. Tag the first release of the project on GitHub with the version number from
   the ``setup.py`` file. For example if the version number in ``setup.py`` is
   0.0.2 then do::

       git tag 0.0.2
       git push --tags


----------------------------------------
Releasing a New Version of ckanext-terria_view
----------------------------------------

ckanext-terria_view is availabe on PyPI as https://pypi.python.org/pypi/ckanext-terria_view.
To publish a new version to PyPI follow these steps:

1. Update the version number in the ``setup.py`` file.
   See `PEP 440 <http://legacy.python.org/dev/peps/pep-0440/#public-version-identifiers>`_
   for how to choose version numbers.

2. Create a source distribution of the new version::

     python setup.py sdist

3. Upload the source distribution to PyPI::

     python setup.py sdist upload

4. Tag the new release of the project on GitHub with the version number from
   the ``setup.py`` file. For example if the version number in ``setup.py`` is
   0.0.2 then do::

       git tag 0.0.2
       git push --tags
