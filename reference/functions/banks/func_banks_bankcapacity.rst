.. _func_banks_bankcapacity:

============
BankCapacity
============

BankCapacity - 

Description
===========

.. code-block:: blitzmax

    BankCapacity( bank:TBank )

Get capacity of bank

The capacity of a bank is the size limit before a bank must allocate
more memory due to a resize. Bank capacity may be increased due to a call
to #ResizeBank by either 50% or the requested amount, whichever is greater.
Capacity never decreases.

Parameters
==========

Return Values
=============

The capacity, in bytes, of the bank's internal memory buffer

Examples
========

See Also
========



