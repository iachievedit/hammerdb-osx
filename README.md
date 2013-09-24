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
*  You may see the following warning when running:
   Wish(6965,0x10bc80000) malloc: *** auto malloc[6965]: error: GC operation on unregistered thread. Thread registered implicitly. Break on auto_zone_thread_registration_error() to debug.
*  You may notice that the menu items are grayed out - we haven't determined the cause but are
   working to resolve it.
*  We've had success with creating a 'tpcc' user specifically for running benchmarks.  
   For example:  
   
   mysql> grant all on tpcc.* to 'tpcc'@'localhost' identified by 'tpccpass';
   mysql> flush privileges;

   If you are running the benchmark against a machine other than localhost you will want to
   update the grant accordingly.
*  While we've tried to provide a package that works "out of the box" (and indeed would like to
   eventually provide a DMG installer), our resources are limited and we've only done 
   out-of-the-box testing on OS X systems that already had MySQL installed, and only against a
   Macbook Pro running OS X 10.7.5 and a Macmini running OS X 10.8.4.
*  Issues can be reported to feedback@iachieved.it, but be aware that it may be some time before
   we can assist.


