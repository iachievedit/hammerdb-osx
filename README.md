HammerDB for OS X 0.1

This is a port of HammerDB, an open source database load testing and benchmarking tool, to
the Mac OS X environment.  Whereas the current version of HammerDB (2.14) supports 
benchmarking against Oracle, MySQL, Postgres, etc., this version only supports MySQL.

Requirements

*  Tcl and Wish must be installed on your Mac (which should be the case for a default
   installation of OS X).
*  libmysqlclient.18.dylib (this can be installed through installing MySQL using
   https://dev.mysql.com/doc/refman/5.5/en/macosx-installation-pkg.html, or using 
   a package manager like Homebrew)

TODO

*  Provide better documentation on installing on a system that does not include MySQL

Notes

*  This package is providing a compiled version of libmysqltcl from a 64-bit Mac.  It
   will not work on a 32-bit system.
   


