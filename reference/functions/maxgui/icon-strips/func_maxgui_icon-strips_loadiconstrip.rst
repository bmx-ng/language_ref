.. _func_maxgui_icon-strips_loadiconstrip:

=============
LoadIconStrip
=============

LoadIconStrip - 

Description
===========

.. code-block:: blitzmax

    LoadIconStrip:TIconStrip(source:Object)

Creates an icon strip from an image file.

An icon strip is a series of small images that can be attached to item-based gadgets.

Icons must be square, and arranged in a single horizontal strip across the source image.

The number of icons in an iconstrip is determined by dividing the image width by its height. For example,
an iconstrip 64 wide by 8 high is assumed to contain 64/8=8 icons.

Once an icon strip has been loaded, it can be attached to item-based gadgets using #SetGadgetIconStrip.

See Also: #SetGadgetIconStrip and #PixmapFromIconStrip

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



