Bash Stub README
================

by Morgan Aldridge <morgant@makkintosshu.com>

OVERVIEW
--------

This is the stub I use for creating new command line tools using `bash`. It's always evolving.

Main features include:

* Informational comment heading
* Parsing command line options & arguments, incl. support for:
	* Single options (e.g. "-h")
	* Single options specified together (e.g. "-tzf")
	* GNU-style long options (e.g. "--help")
	* GNU-style long options using alternate value format (e.g. "--dry-run=off")
* Help, version, and verbose options

WHY NOT GETOPT/GETOPTS?
-----------------------

`getopt` & `getopts` can greatly simplify parsing command line options & arguments, but both have limitations that I don't want to be stuck with. I'd like to have the best of both options, plus additional features, and I've been able to get that by rolling my own options & argument parsing.

`getopt` supports single options (e.g. "-h"), single options specified together (e.g. "-tzf"), and GNU-style long options (e.g. "--help"), but doesn't support white space in arguments, even when escaped, on many platforms. Many (all?) versions of Mac OS X are afflicted by this, plus Mac file systems have always supported spaces in file names, greatly increasing the likelihood of running into that limitation.

`getopts` supports quoted arguments, but does not support GNU-style long options (e.g. "--help"). While long options can be lived without, I find that they help further clarify a tool's documentation and make it easier to test & troubleshoot a tool's various options with fewer mistakes.

LICENSE
-------

Copyright (c) 2012, Morgan Aldridge
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
