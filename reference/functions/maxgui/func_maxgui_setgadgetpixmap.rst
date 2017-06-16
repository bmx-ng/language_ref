.. _func_maxgui_setgadgetpixmap:

===============
SetGadgetPixmap
===============

SetGadgetPixmap - 

Description
===========

.. code-block:: blitzmax

    SetGadgetPixmap( gadget:TGadget, pixmap:TPixmap, flags% = GADGETPIXMAP_ICON )

Set a gadget's pixmap.
This is a more generic form of old backwards-compatible #SetPanelPixmap function which now allows icons
to be set for other gadgets as well as just backgrounds for panels.

For setting background pixmaps on panels, @flags should still be one of the following:

[ @Flag | @Meaning
* PANELPIXMAP_TILE | The panel is filled with repeating tiles.
* PANELPIXMAP_CENTER | The pixmap is positioned at the center of the panel.
* PANELPIXMAP_FIT | The pixmap is scaled proportionally to best fit the panel size.
* PANELPIXMAP_FIT2 | A variant of PANELPIXMAP_FIT where clipping can occur to achieve a better fit.
* PANELPIXMAP_STRETCH | The pixmap is stretched to fit the entire panel.
]

Alternatively, to set a push-button or menu's icon, use the following constants:

[ @Flag | @Meaning
* GADGETPIXMAP_ICON | Places an icon-sized pixmap onto a button/menu.
* GADGETPIXMAP_NOTEXT | Removes text on buttons when used in conjunction with GADGETPIXMAP_ICON.
]

Each platform allows slightly different maximum icon sizes for their menus. Therefore, the recommended
size for menu icons is 12x12 pixels, which appears to work well on all supported platforms.

Note: At present, OK buttons cannot have an icon set as a cross-platform solution is unavailable.

The function can be passed #Null as the parameter for @pixmap, in which case the pixmap will be removed.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



