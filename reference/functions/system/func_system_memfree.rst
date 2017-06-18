.. _func_system_memfree:

=======
MemFree
=======

MemFree - Free allocated memory

Description
===========

.. code-block:: blitzmax

    MemFree( mem:Byte Ptr )

A block of memory specified by ``mem``, having been previously allocated by :ref:`func_system_memalloc` or
:ref:`func_system_memextend` is freed, making it available for further allocations.

Parameters
==========

* ``mem`` - A pointer to an allocated memory block.

Return Values
=============

Nothing.

Examples
========

See Also
========

:ref:`func_system_memalloc`, :ref:`func_system_memextend`, :ref:`func_system_memcopy`, :ref:`func_system_memmove`, :ref:`func_system_memclear`
