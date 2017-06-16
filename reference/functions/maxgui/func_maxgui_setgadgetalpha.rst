.. _func_maxgui_setgadgetalpha:

==============
SetGadgetAlpha
==============

SetGadgetAlpha - 

Description
===========

.. code-block:: blitzmax

    SetGadgetAlpha( gadget:TGadget,alpha# )

Set the transparency of a gadget.
Alpha should be in the range 0.0 (invisible) to 1.0 (solid). Very few gadgets support this functionality,
but some Mac OS X gadgets do, in addition to @Windows when running Windows XP+. In certain circumstances, window
transparency may be disabled (for example, when a canvas is added to a window) to prevent redraw issues on some
platforms.

Using the function on windows with @Canvases on them may cause undesired effects, particularly on Windows 2000/XP
because of conflicts between the software based window manager and the hardware accelerated graphics contexts.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



