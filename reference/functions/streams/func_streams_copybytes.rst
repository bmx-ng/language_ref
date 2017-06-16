.. _func_streams_copybytes:

=========
CopyBytes
=========

CopyBytes - 

Description
===========

.. code-block:: blitzmax

    CopyBytes( fromStream:TStream,toStream:TStream,count,bufSize=4096 )

Copy bytes from one stream to another

#CopyBytes copies @count bytes from @fromStream to @toStream.

A #TStreamReadException is thrown if not all bytes could be read, and a
#TStreamWriteException is thrown if not all bytes could be written.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



