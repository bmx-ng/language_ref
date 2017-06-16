.. _func_event_waitevent:

=========
WaitEvent
=========

WaitEvent - 

Description
===========

.. code-block:: blitzmax

    WaitEvent()

Get the next event from the event queue, waiting if necessary

#WaitEvent removes an event from the event queue and updates the #CurrentEvent
global variable.

If there are no events in the event queue, #WaitEvent halts program execution until
an event is available.

Parameters
==========

Return Values
=============

The id of the next event in the event queue

Examples
========

See Also
========



