.. _func_event_waittimer:

=========
WaitTimer
=========

WaitTimer - 

Description
===========

.. code-block:: blitzmax

    WaitTimer( timer:TTimer )

Wait until a timer ticks

Parameters
==========

Return Values
=============

The number of ticks since the last call to #WaitTimer

Examples
========

.. code-block:: blitzmax

    timer=CreateTimer( 10 )
    
    Repeat
        Print "Ticks="+WaitTimer( timer )
    Forever

See Also
========



