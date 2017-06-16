.. _func_banks_lockbank:

========
LockBank
========

LockBank - 

Description
===========

.. code-block:: blitzmax

    LockBank:Byte Ptr( bank:TBank )

Lock a bank's memory block

While locked, a bank cannot be resized.

After you have finished with a bank's memory block, you must use #UnlockBank
to return it to the bank.

Parameters
==========

Return Values
=============

A byte pointer to the memory block controlled by the bank.

Examples
========

See Also
========



