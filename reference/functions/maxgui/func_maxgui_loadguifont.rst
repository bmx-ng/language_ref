.. _func_maxgui_loadguifont:

===========
LoadGuiFont
===========

LoadGuiFont - 

Description
===========

.. code-block:: blitzmax

    LoadGuiFont:TGuiFont(name$,height:Double,bold=False,italic=False,underline=False,strikethrough=False)

Load a system font by name.

Loads a system font by name and returns and object that can be used with the #SetGadgetFont command.

Depending on the platform, some gadgets may not respond to all or any of the attributes specified.

See Also: #RequestFont, #LookupGuiFont, #FontName, #FontSize and #FontStyle

Parameters
==========

Return Values
=============

A @TGuiFont object, or #Null if a suitable matching font was not found on the system.

Examples
========

See Also
========



