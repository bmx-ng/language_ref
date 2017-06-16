.. _func_graphics_pixmaps_createstaticpixmap:

==================
CreateStaticPixmap
==================

CreateStaticPixmap - 

Description
===========

.. code-block:: blitzmax

    CreateStaticPixmap:TPixmap( pixels:Byte Ptr,width,height,pitch,format )

Create a pixmap with existing pixel data

The memory referenced by a static pixmap is not released when the pixmap is deleted.

See #CreatePixmap for valid pixmap formats.

Parameters
==========

Return Values
=============

A new pixmap object that references an existing block of memory

Examples
========

See Also
========



