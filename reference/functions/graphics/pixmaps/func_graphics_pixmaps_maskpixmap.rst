.. _func_graphics_pixmaps_maskpixmap:

==========
MaskPixmap
==========

MaskPixmap - 

Description
===========

.. code-block:: blitzmax

    MaskPixmap:TPixmap( pixmap:TPixmap,mask_red,mask_green,mask_blue ) NoDebug

Mask a pixmap
@MaskPixmap builds a new pixmap with alpha components set to '0' wherever the pixel colors
in the original @pixmap match @mask_red, @mask_green and @mask_blue. @mask_red, @mask_green and @mask_blue
should be in the range 0 to 255.

Parameters
==========

Return Values
=============

A new pixmap object

Examples
========

See Also
========



