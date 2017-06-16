.. _func_streams_readline:

========
ReadLine
========

ReadLine - 

Description
===========

.. code-block:: blitzmax

    ReadLine$( stream:TStream )

Read a line of text from a stream

Bytes are read from @stream until a newline character (ascii code 10) or null
character (ascii code 0) is read, or end of file is detected.

Carriage Return characters (ascii code 13) are silently ignored.

The bytes read are returned in the form of a string, excluding any terminating newline
or null character.

Parameters
==========

Return Values
=============

A string

Examples
========

See Also
========



