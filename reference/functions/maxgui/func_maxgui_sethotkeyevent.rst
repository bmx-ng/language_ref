.. _func_maxgui_sethotkeyevent:

==============
SetHotKeyEvent
==============

SetHotKeyEvent - 

Description
===========

.. code-block:: blitzmax

    SetHotKeyEvent:THotKey( key,mods,event:TEvent=Null,owner=0 )

Set a hotkey event.

When the specified hotkey combination is selected by the user, the specified
@event will be emitted using #EmitEvent.

If @event is #Null, an event with @id equal to EVENT_HOTKEYHIT, @data equal
to @key and @mods equal to @mods will be emitted.

#SetHotKeyEvent will overwrite any existing hotkey event with the same @key, @mods and @owner.

Please refer to the #{key codes} module for valid key and modifier codes.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



