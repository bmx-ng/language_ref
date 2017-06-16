.. _func_maxgui_menus_windowmenu:

==========
WindowMenu
==========

WindowMenu - 

Description
===========

.. code-block:: blitzmax

    WindowMenu:TGadget( window:TGadget )

Get a window's main-menu handle.
Required when a menu is to be added to a window using #CreateMenu. This function
should @not be used for sub-menus under any circumstance.

It should also be mentioned that when creating popup menus this function isn't required - instead
#Null should be passed as the parent of the root popup menu.
See Also: #CreateMenu and #UpdateWindowMenu

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



