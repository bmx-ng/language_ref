.. _func_event_runhooks:

========
RunHooks
========

RunHooks - 

Description
===========

.. code-block:: blitzmax

    RunHooks:Object( id,data:Object )

Run hook functions

#RunHooks runs all hook functions that have been added for the specified hook @id.

The first hook function is called with the provided @data object. The object returned by
this function is then passed as the @data parameter to the next hook function and so on.
Therefore, hook functions should generally return the @data parameter when finished.

Parameters
==========

Return Values
=============

The data produced by the last hook function

Examples
========

See Also
========



