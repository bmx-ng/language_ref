.. _func_streams_copystream:

==========
CopyStream
==========

CopyStream - 

Description
===========

.. code-block:: blitzmax

    CopyStream( fromStream:TStream,toStream:TStream,bufSize=4096 )

Copy stream contents to another stream

#CopyStream copies bytes from @fromStream to @toStream Until @fromStream reaches end
of file.

A #TStreamWriteException is thrown if not all bytes could be written.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



