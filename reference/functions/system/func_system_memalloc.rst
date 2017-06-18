.. _func_system_memalloc:

========
MemAlloc
========

MemAlloc - Allocate memory

Description
===========

.. code-block:: blitzmax

    MemAlloc:Byte Ptr( size:Size_T )

Allocates a block of ``size`` bytes of memory, returning a pointer to the start of the block.

The content of the newly allocated block remains uninitialised, and therefore has indeterminate values.

Parameters
==========

* ``size`` - Size of the block of memory, in bytes.

Return Values
=============

A new block of memory ``size`` bytes long.

Examples
========

See Also
========

:ref:`func_system_memextend`, :ref:`func_system_memmove`, :ref:`func_system_memcopy`, :ref:`func_system_memfree`, :ref:`func_system_memclear`
