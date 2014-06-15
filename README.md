isbnutil
========

Tiny ISBN utilities.

License
-------

zlib License.

Target environments
-------------------

Cygwin, Linux, Mac OS X.

isbnutil is shell script (sh), and so probably worked in other Unix-like environment.

Set up
------

Put isbnutil in a directory registered in PATH.

Usage
-----

Please check help message `isbnutil -h`

Example
-------

    $ # The Unix Programming Environment
    $ #   by Brian W. Kernighan, Rob Pike
    $ # ISBN-10: 013937681X
    $ # ISBN-13: 978-0139376818
    $
    $ isbnutil cksum 013937681
    X
    $ isbnutil cksum 978013937681
    8
    $ isbnutil convert 013937681X
    9780139376818
    $ isbnutil convert 9780139376818
    013937681X
    $ isbnutil test 013937681X && echo valid ISBN format
    valid ISBN format
    $ isbnutil test 0139376810 || echo invalid ISBN format
    invalid ISBN format
    $ isbnutil type 013937681X
    10
    $ isbnutil type 9780139376818
    13
    $ isbnutil type 0139376810
    none
    $ _
