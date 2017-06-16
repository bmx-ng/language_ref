.. _func_system_pollsystem:

==========
PollSystem
==========

PollSystem - 

Description
===========

.. code-block:: blitzmax

    PollSystem()

Poll operating system

#PollSystem returns control back to the operating system, allowing such
events as keystrokes and gadget actions to be processed. Control is then
returned back to your program.

If #PollSystem encounters a key, mouse or app suspend/resume/terminate
event, an equivalent #TEvent object event will be generated which may be intercepted using
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



