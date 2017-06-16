.. _func_graphics_max2d_sethandle:

=========
SetHandle
=========

SetHandle - 

Description
===========

.. code-block:: blitzmax

    SetHandle( x#,y# )

Set drawing handle

The drawing handle is a 2D offset subtracted from the x,y location of all
drawing commands except #DrawImage as Images have their own unique handles.

Unlike #SetOrigin the drawing handle is subtracted before rotation and scale
are applied providing a 'local' origin.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



