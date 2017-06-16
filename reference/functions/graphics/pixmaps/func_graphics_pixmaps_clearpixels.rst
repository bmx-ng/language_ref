.. _func_graphics_pixmaps_clearpixels:

===========
ClearPixels
===========

ClearPixels - 

Description
===========

.. code-block:: blitzmax

    ClearPixels( pixmap:TPixmap,argb=0 )

Clear a pixmap

Sets all pixels in a pixmap to a 32 bit pixel value.

The 32 bit @argb value contains the following components:

[ bits 24-31 | pixel alpha
* bits 16-23 | pixel red
* bits 8-15 | pixel green
* bits 0-7 | pixel blue
]

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



