.. _func_zlib_compress2:

=========
compress2
=========

compress2 - Compress data at a specified level.

Description
===========

.. code-block:: blitzmax

    ?win32 Or ptr32
        Function compress2:Int( dest:Byte Ptr, dest_len:UInt Var, source:Byte Ptr, source_len:UInt, level:Int )
    ?ptr64 And Not win32
        Function compress2:Int( dest:Byte Ptr, dest_len:ULong Var, source:Byte Ptr, source_len:ULong, level:Int )
    ?

Attempts to compress ``source_len`` bytes of data in the buffer ``source``, placing the result in the buffer ``dest``, at the
level described by ``level``. The level supplied should be a value between 0 and 9.
A level of 1 requests the highest speed, while a level of 9 requests the highest compression. A level of 0 indicates
that no compression should be used, and the output shall be the same as the input.

On entry, ``dest_len`` should point to a value describing the size of the ``dest`` buffer. The application should
ensure that this value be at least ``(source_len * 1.001) + 12``. On successful exit, the variable referenced by
``dest_len`` will be updated to hold the length of compressed data in dest.

Parameters
==========

* ``dest`` - The destination buffer.
* ``dest_len`` - The size of the destination buffer. On exit, will hold the actual size of the compressed data.
* ``source`` - The source buffer.
* ``source_len`` - The size of the source data.
* ``level`` - The required compression level, 0 to 9, where 0 is none, 9 is maximum.



Return Values
=============

On success, returns 0. Otherwise a value to indicate the error.

Examples
========

See Also
========

:ref:`func_zlib_compress`
