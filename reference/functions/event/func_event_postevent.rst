.. _func_event_postevent:

=========
PostEvent
=========

PostEvent - 

Description
===========

.. code-block:: blitzmax

    PostEvent( event:TEvent,update=False )

Post an event to the event queue
#PostEvent adds an event to the end of the event queue.

The @update flag can be used to update an existing event. If @update is True
and an event with the same @id and @source is found in the event
queue, the existing event will be updated instead of @event
being added to the event queue. This can be useful to prevent high frequency
events such as timer events from flooding the event queue.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



