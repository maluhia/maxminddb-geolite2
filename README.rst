maxminddb-geolite2
==================

Description
-----------

maxminddb-geolite2 is a library that provides access to MaxMind's GeoIP2
databases.  It depends on the official MaxMind library for functionality,
but it conveniently ships a recent version of the GeoLite2 City database
as provided by MaxMind.

This fork uses Country data instead of City.

This package includes GeoLite2 data created by MaxMind, available from
`maxmind.com <http://www.maxmind.com>`_ under the Creative Commons
Attribution-ShareAlike 3.0 Unported License.

Installation
------------

You can get the library directly from this github repo:

.. code-block:: bash

    $ sudo pip3 install -e git+https://github.com/maluhia/maxminddb-geolite2.git#egg=maxminddb-geolite2


Usage
-----

Once you have installed the ``maxminddb-geolite2`` package you can start
using the database straight away:

.. code-block:: pycon

    >>> from geolite2 import geolite2
    >>>
    >>> reader = geolite2.reader()
    >>> reader.get('1.1.1.1')
    {'country': ... }
    >>>
    >>> geolite2.close()
