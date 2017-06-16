.. _func_maxgui_pixmapfromiconstrip:

===================
PixmapFromIconStrip
===================

PixmapFromIconStrip - 

Description
===========

.. code-block:: blitzmax

    PixmapFromIconStrip:TPixmap(iconstrip:TIconStrip, index = -1)

Returns a pixmap containing either a copy of the original icon-strip or just the specified icon.
@iconstrip: The icon-strip to return a pixmap from.

@index: The index (base 0) of the icon to extract. If this is negative, a %copy of the
original pixmap used to create the iconstrip is returned.

This function will return #Null if no iconstrip is passed, or if the icon index is invalid.

See Also: #LoadIconStrip

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



