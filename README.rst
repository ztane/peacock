===================================
Peacock
===================================
Peacock is Extraordinary Arbitrary Command Output Colouring Kit
-----------------------------------

SYNOPSIS
--------

peacock command [arg1 .. argN]


DESCRIPTION
-----------

Peacock is a regular expression based colour formatter for programs that
display output on the command-line. It works as a wrapper around the
target program, executing it *in a pseudo terminal*. This means that
it is possible to colourise programs that take full control of the terminal.

Peacock applies matching rules to patterns in the output and applies
colour sets to those matches. If the $ACOC environment variable is set to
'none', Peacock will not perform any colouring.


DEPENDENCIES
------------

*   Python 3
*   ANSI Terminal
*   *NIX

Usage
-----

*   Run any command, but coloured with ANSI colours: ``peacock command ordinary arguments``.

*   Peacock needs acoc.conf to work; see docs/acoc.conf.html
    for more info and docs/acoc.conf for a boilerplate config.


OPTIONS
-------

None exist

AUTHOR
------

Pythonized by Antti Haapala <antti@haapala.name>

PTY code adapted from sample by Joshua D. Bartlett

Idea, original documentation and original Ruby version by Ian Macdonald <ian@caliban.org>
                                   
COPYRIGHT
---------

Copyright (C) 2013-2016 Antti Haapala

Original Ruby Code and configuration Copyright (C) 2003-2004 Ian Macdonald

Licensed under GPLv3.

This is free software; see the source for copying conditions.
There is NO warranty; not even for MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE.

FILES
-----

* acoc.conf 
* /usr/local/etc/acoc.conf
* /etc/acoc.conf
* ~/.acoc.conf

ENVIRONMENT
-----------

``$ACOCRC``
           If set, this specifies the location of an additional configuration
           file.

CONTRIBUTING
------------

Peacock is only as good as the configuration file that it uses. If you
compose pattern-matching rules that you think would be useful to other
people, please send them to me for inclusion in a subsequent release.

SEE ALSO
--------

* acoc.conf
* acoc home page - http://www.caliban.org/ruby/

BUGS
----

* Nested regular expressions do not work well. Inner subexpressions need
  to use clustering ``(?:)``, not capturing ``()``. In other words, they can be
  used for matching, but not for colouring.
