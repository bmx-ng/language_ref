.. _func_maxgui_setgadgetsensitivity:

====================
SetGadgetSensitivity
====================

SetGadgetSensitivity - 

Description
===========

.. code-block:: blitzmax

    SetGadgetSensitivity( gadget:TGadget, flags )

Sets whether a standard MaxGUI gadget emits events from the keyboard or mouse.
This functions attempts to provide similar functionality for all gadgets to that of @Panels created with the PANEL_ACTIVE flag.

The @flags parameter can be any combination of the following:

SENSITIZE_MOUSE: The gadget will emit the following events:

[ @{Event ID} | @Description
* EVENT_MOUSEDOWN | Mouse button pressed. Event data contains mouse button code.
* EVENT_MOUSEUP | Mouse button released. Event data contains mouse button code.
* EVENT_MOUSEMOVE | Mouse moved. Event x and y contain mouse coordinates.
* EVENT_MOUSEWHEEL | Mouse wheel spun. Event data contains delta clicks.
* EVENT_MOUSEENTER | Mouse entered gadget area.
* EVENT_MOUSELEAVE | Mouse left gadget area.
]

SENSITIZE_KEYS: The gadget will emit the following events:

[ @{Event ID} | @Description
* EVENT_KEYDOWN | Key pressed. Event data contains keycode.
* EVENT_KEYUP | Key released. Event data contains keycode.
* EVENT_KEYREPEAT | Key is being held down. Event data contains keycode.
]

SENSITIZE_ALL: Exactly the same as combining SENSITIZE_MOUSE and SENSITIZE_KEYS.

Gadgets that have been disabled should not emit key events, although they may still emit mouse events.

Not all gadgets will be able to emit all of the events, particularly those that don't receive typical focus
such as labels or htmlviews, but even this may differ depending on the platform.

%{@Warning: This is a powerful new function that possibly involves hooking into the system's message queue
to ask for mouse/key events before they are processed even by the OS's GUI library. As such, using this function
on certain controls may cause them to be behave differently. In addition, care should be taken when using
this function to avoid infinite loops, for example repositioning gadgets in an event hook that processes the
message as it is received.

As a result, it is to be recommended that this function is only used by advanced MaxGUI users.

See Also: #GadgetSensitivity

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



