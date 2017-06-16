.. _func_event_pollevent:

=========
PollEvent
=========

PollEvent - 

Description
===========

.. code-block:: blitzmax

    PollEvent()

Get the next event from the event queue

#PollEvent removes an event from the event queue and updates the #CurrentEvent
global variable.

If there are no events in the event queue, #PollEvent returns 0.

Parameters
==========

Return Values
=============

The id of the next event in the event queue, or 0 if the event queue is empty

Examples
========

See Also
========



