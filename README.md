isbnutil
========

Tiny ISBN utilities.

License
-------

zlib License.

Target environments
-------------------

Cygwin, Linux, macOS.

isbnutil is shell script (sh), and so probably works fine on other Unix-like environment.

Set up
------

Put isbnutil in a directory registered in PATH.

Usage
-----

Please check help message `isbnutil -h`

Example
-------

```sh
# The Unix Programming Environment
#   by Brian W. Kernighan, Rob Pike
# ISBN-10: 013937681X
# ISBN-13: 978-0139376818

# isbnutil cksum <ISBN without check digit>
isbnutil cksum 013937681
#=> X
isbnutil cksum 978013937681
#=> 8

# isbnutil convert <ISBN>
isbnutil convert 013937681X
#=> 9780139376818
isbnutil convert 9780139376818
#=> 013937681X

# isbnutil test <ISBN>
isbnutil test 013937681X && echo valid ISBN format
#=> valid ISBN format
isbnutil test 0139376810 || echo invalid ISBN format
#=> invalid ISBN format

# isbnutil type <ISBN>
isbnutil type 013937681X
#=> 10
isbnutil type 9780139376818
#=> 13
isbnutil type 0139376810
#=> none
```
