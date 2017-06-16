.. _func_graphics_max2d_lockimage:

=========
LockImage
=========

LockImage - 

Description
===========

.. code-block:: blitzmax

    LockImage:TPixmap( image:TImage,frame=0,read_lock=True,write_lock=True )

Lock an image for direct access

Locking an image allows you to directly access an image's pixels.

Only images created with the DYNAMICIMAGE flag can be locked.

Locked images must eventually be unlocked with #UnlockImage before they can be drawn.

Parameters
==========

Return Values
=============

A pixmap representing the image contents

Examples
========

See Also
========



