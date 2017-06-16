.. _func_graphics_pixmaps_createpixmap:

============
CreatePixmap
============

CreatePixmap - 

Description
===========

.. code-block:: blitzmax

    CreatePixmap:TPixmap( width,height,format,align_bytes=4 )

Create a pixmap

@format should be one of the following:

[ @Format | @Description
* PF_A8 | 8 bit alpha
* PF_I8 | 8 bit intensity
* PF_RGB888 | 24 bit big endian RGB
* PF_BGR888 | 24 bit little endian RGB
* PF_RGBA8888 | 32 bit big endian RGB with alpha
* PF_BGRA8888 | 32 bit little endian RGB with alpha
]

Note that the newly created pixmap will contain random data. #ClearPixels can
be used to set all pixels to a known value prior to use.

Parameters
==========

Return Values
=============

A new pixmap object of the specified @width and @height

Examples
========

See Also
========



