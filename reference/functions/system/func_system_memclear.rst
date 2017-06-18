.. _func_system_memclear:

========
MemClear
========

MemClear - Clear a block of memory to 0

Description
===========

.. code-block:: blitzmax

    MemClear( mem:Byte Ptr, size:Size_T )

Clears ``size`` bytes of the block of ``mem`` memory to zero.

Parameters
==========

* ``mem`` - A pointer to the block of memory to clear.
* ``size`` - Number of bytes to set to 0.

Return Values
=============

Nothing.

Examples
========

See Also
========

:ref:`func_system_memalloc`, :ref:`func_system_memextend`, :ref:`func_system_memcopy`, :ref:`func_system_memmove`, :ref:`func_system_memfree`
