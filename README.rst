pgbackup
========

About
-----

CLI for backup remote PostgreSQL database either locally or to S3. Code from the Linux Academy course:  `Python 3 Scripting for System Administrators <https://linuxacademy.com/cp/modules/view/id/168>`_


Preparing the Development
-------------------------

1. Clone repository: ``git clone git@github.com:example/pgbackup``
2. ``cd`` into the repository.
3. Fetch development dependencies ``pip install -r requirements-dev.txt``
4. Activate virtualenv: ``source venv/bin/activate``

Usage
-----

Pass in a full database URL, the storage driver, and the destination.

S3 Example w/ bucket name:

::

    $ pgbackup postgres://bob@example.com:5432/db_one --driver s3 backups

Local Example w/ local path:

::

    $ pgbackup postgres://bob@example.com:5432/db_one --driver local /var/local/db_one/bakcups/dump.sql

Running Tests
-------------

Run tests locally using ``make`` if virtualenv is active:

::

    $ pytest -vv
