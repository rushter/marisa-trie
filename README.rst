marisa-trie
===========

A fork of `marisa-trie <https://github.com/pytries/marisa-trie>`_ that support Python 3.9.

Static memory-efficient Trie-like structures for Python (2.7 and 3.4+)
based on `marisa-trie`_ C++ library.

String data in a MARISA-trie may take up to 50x-100x less memory than
in a standard Python dict; the raw lookup speed is comparable; trie also
provides fast advanced methods like prefix search.

.. note::

    There are official SWIG-based Python bindings included
    in C++ library distribution; this package provides alternative
    Cython-based pip-installable Python bindings.

.. _marisa-trie: https://github.com/s-yata/marisa-trie

Installation
============

::

    pip install marisa-trie-m


Current limitations
===================

* The library is not tested with mingw32 compiler;
* ``.prefixes()`` method of ``BytesTrie`` and ``RecordTrie`` is quite slow
  and doesn't have iterator counterpart;
* ``read()`` and ``write()`` methods don't work with file-like objects
  (they work only with real files; pickling works fine for file-like objects);
* there are ``keys()`` and ``items()`` methods but no ``values()`` method.

License
=======

Wrapper code is licensed under MIT License.

Bundled `marisa-trie`_ C++ library is dual-licensed under
LGPL and BSD 2-clause license.
