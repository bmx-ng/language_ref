.. _func_event_createtimer:

===========
CreateTimer
===========

CreateTimer - 

Description
===========

.. code-block:: blitzmax

    CreateTimer:TTimer( hertz#,event:TEvent=Null )

Create a timer

#CreateTimer creates a timer object that 'ticks' @hertz times per second.

Each time the timer ticks, @event will be emitted using #EmitEvent.

If @event is Null, an event with an @id equal to EVENT_TIMERTICK and
@source equal to the timer object will be emitted instead.

Parameters
==========

Return Values
=============

A new timer object

Examples
========

See Also
========



