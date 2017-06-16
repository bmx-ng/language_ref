.. _func_system_waitsystem:

==========
WaitSystem
==========

WaitSystem - 

Description
===========

.. code-block:: blitzmax

    WaitSystem()

Wait for operating system

#WaitSystem returns control back to the operating system, waiting until
an event such as a keystroke or gadget action occurs.

Note that #WaitSystem may wait indefinitely if there is no possibility
of any events occuring, so use with caution.

If #WaitSystem encounters a key, mouse or app suspend/resume/terminate
event, an equivalent #TEvent object will be generated which may be intercepted using
the #EmitEventHook hook.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



