.. _func_system_memmove:

=======
MemMove
=======

MemMove - Move a block of memory

Description
===========

.. code-block:: blitzmax

    MemMove( dst:Byte Ptr, src:Byte Ptr, size:Size_T )

Copies a potentially overlapping block of ``size`` bytes from the location pointed by ``src`` to the
block of memory pointed to by ``dst``.

Parameters
==========

* ``dst`` - A pointer to the destination memory where the content is to be copied.
* ``src`` - A pointer to the source data to be copied.
* ``size`` - The number of bytes to copy.

Return Values
=============

Nothing.

Examples
========

See Also
========

:ref:`func_system_memalloc`, :ref:`func_system_memextend`, :ref:`func_system_memcopy`, :ref:`func_system_memfree`, :ref:`func_system_memclear`
