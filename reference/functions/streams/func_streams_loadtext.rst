.. _func_streams_loadtext:

========
LoadText
========

LoadText - 

Description
===========

.. code-block:: blitzmax

    LoadText$( url:Object )

Load text from a stream

#LoadText loads LATIN1, UTF8 or UTF16 text from @url.

The first bytes read from the stream control the format of the text:
[ &$fe $ff | Text is big endian UTF16
* &$ff $fe | Text is little endian UTF16
* &$ef $bb $bf | Text is UTF8
]

If the first bytes don't match any of the above values, the stream
is assumed to contain LATIN1 text.

Parameters
==========

Return Values
=============

A string containing the text

Examples
========

See Also
========



