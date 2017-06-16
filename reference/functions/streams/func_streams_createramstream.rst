.. _func_streams_createramstream:

===============
CreateRamStream
===============

CreateRamStream - 

Description
===========

.. code-block:: blitzmax

    CreateRamStream:TRamStream( ram:Byte Ptr,size,readable,writeable )

Create a ram stream
A ram stream allows you to read and/or write data directly from/to memory.
A ram stream extends a stream object so can be used anywhere a stream is expected.

Be careful when working with ram streams, as any attempt to access memory
which has not been allocated to your application can result in a runtime crash.

Parameters
==========

Return Values
=============

A ram stream object

Examples
========

See Also
========



