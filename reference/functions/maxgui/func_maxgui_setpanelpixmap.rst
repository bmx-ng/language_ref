.. _func_maxgui_setpanelpixmap:

==============
SetPanelPixmap
==============

SetPanelPixmap - 

Description
===========

.. code-block:: blitzmax

    SetPanelPixmap( panel:TGadget,pixmap:TPixmap,flags=PANELPIXMAP_TILE)

Set panel's background image to a pixmap.
Can be used instead of #SetGadgetPixmap for backwards compatability.

[ @Flags | @Meaning
* PANELPIXMAP_TILE | The panel is filled with repeating tiles.
* PANELPIXMAP_CENTER | The pixmap is positioned at the center of the panel.
* PANELPIXMAP_FIT | The pixmap is scaled to best fit the panel size.
* PANELPIXMAP_FIT2 | A variant of PANELPIXMAP_FIT where clipping can occur to achieve a better fit.
* PANELPIXMAP_STRETCH | The pixmap is stretched to fit the entire panel.
]

The function can be passed 'Null' as the parameter for @pixmap, in which case the pixmap should be removed.

See Also: #CreatePanel and #SetPanelColor

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



