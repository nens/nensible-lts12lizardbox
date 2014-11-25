N&S LTS 12.04 lizard base box
=============================

All the common requirements of a regular lizard4-like site on an ubuntu 12.04
LTS base. "Regular lizard4" means a django 1.4+ that is OK with most of the
dependencies (like mapnik) as provided by the LTS. The goal is not to litter
the base box with PPAs and custom packages.

**One exception** is being made: the ubuntugis-stable PPA is used as the gdal
version of the LTS is really too old


What does the role mean?
------------------------

If a server has this role, it is a pretty standard common-at-N&S box. You
could put a lizard4 site or TRS on it. The kind of configuration you'd use to
run jenkins on: lizard-map and trs and lizard-security should be able to run
``bin/test`` on them (apart from additionally needing to install jenkins and a
database server).

In the case of a jenkins box, you'd might have to install some extra packages.

In any case, it isn't a wildly modified "PPA-invested" box.


Requirements
------------

It is build upon ubuntu's 12.04 LTS release. When a new LTS comes out it is
probably a good time to make a new one specifically for that LTS: a nice
cleanup instead of bolting "if/else" statements onto this role.

Note: an LTS14 box is available: https://github.com/nens/nensible-lts14lizardbox


Example playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too::

    - hosts: servers
      roles:
         - nensible-ltx12lizardbox


License
-------

BSD


Author Information
------------------

Created by `Reinout van Rees <http://reinout.vanrees.org>`_ at `Nelen &
Schuurmans <http://www.nelen-schuurmans.nl>`_.
