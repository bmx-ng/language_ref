.. _func_input_appterminate:

============
AppTerminate
============

AppTerminate - 

Description
===========

.. code-block:: blitzmax

    AppTerminate()

Return app terminate state

Parameters
==========

Return Values
=============

True if user has requested to terminate application

Examples
========

.. code-block:: blitzmax

    Graphics 640,480,0
    
    While Not AppTerminate() Or Not Confirm( "Terminate?" )
    
        Cls
        DrawText MouseX()+","+MouseY(),0,0
        Flip
    
    Wend

See Also
========



