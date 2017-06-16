.. _func_streams_createsocketstream:

==================
CreateSocketStream
==================

CreateSocketStream - 

Description
===========

.. code-block:: blitzmax

    CreateSocketStream:TSocketStream( socket:TSocket,autoClose=True )

Create a socket stream

A socket stream allows you to treat a socket as if it were a stream.

If @autoClose is true, @socket will be automatically closed when the socket
stream is closed. Otherwise, it is up to you to somehow close @socket at
a later time.

Parameters
==========

Return Values
=============

A new socket stream

Examples
========

See Also
========



