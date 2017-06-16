.. _func_graphics_pixmaps_readpixel:

=========
ReadPixel
=========

ReadPixel - 

Description
===========

.. code-block:: blitzmax

    ReadPixel( pixmap:TPixmap,x,y )

Read a pixel from a pixmap

The returned 32 bit value contains the following components:

[ bits 24-31 | pixel alpha
* bits 16-23 | pixel red
* bits 8-15 | pixel green
* bits 0-7 | pixel blue
]

Parameters
==========

Return Values
=============

A 32 bit pixel value

Examples
========

See Also
========



