.. _func_system_onend:

=====
OnEnd
=====

OnEnd - 

Description
===========

.. code-block:: blitzmax

    OnEnd( fun() )

Add a function to be called when the program ends
#OnEnd allows you to specify a function to be called when the program ends. OnEnd functions are called
in the reverse order to that in which they were added.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' onend.bmx
    
    Function cleanup()
    Print "cleaning up"
    End Function
    
    OnEnd cleanup
    Print "program running"
    End    'the cleanup function will be called at this time

See Also
========



