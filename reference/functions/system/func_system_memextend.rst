.. _func_system_memextend:

=========
MemExtend
=========

MemExtend - Extend a block of memory

Description
===========

.. code-block:: blitzmax

    MemExtend:Byte Ptr( mem:Byte Ptr, size:Size_T, new_size:Size_T )

Copies an existing block of memory specified by ``mem`` and ``size`` into a new block
of memory ``new_size`` bytes long. The existing block is released and the new block is returned.

Parameters
==========

* ``mem`` - A pointer to the source data to be copied.
* ``size`` - The number of bytes to copy to the new block.
* ``new_size`` - The total number of bytes to allocate to the new block.

Return Values
=============

A new block of memory ``new_size`` bytes long.

Examples
========

See Also
========

:ref:`func_system_memalloc`, :ref:`func_system_memmove`, :ref:`func_system_memcopy`, :ref:`func_system_memfree`, :ref:`func_system_memclear`
