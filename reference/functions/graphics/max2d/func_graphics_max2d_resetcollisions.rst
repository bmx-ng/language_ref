.. _func_graphics_max2d_resetcollisions:

===============
ResetCollisions
===============

ResetCollisions - 

Description
===========

.. code-block:: blitzmax

    ResetCollisions(mask%=0)

Clears collision layers specified by the value of @mask, mask=0 for all layers.

The BlitzMax 2D collision system manages 32 layers, the @mask parameter can
be a combination of the following values or the special value COLLISION_LAYER_ALL in order
to perform collision operations on multiple layers.

Note: COLLISION_LAYER_32 is used by the #ImagesCollide and #ImagesCollide2 commands.

[ @Layer | @{Mask value}
* COLLISION_LAYER_ALL | 0
* COLLISION_LAYER_1 | $0001
* COLLISION_LAYER_2 | $0002
* COLLISION_LAYER_3 | $0004
* COLLISION_LAYER_4 | $0008
* COLLISION_LAYER_5 | $0010
* COLLISION_LAYER_6 | $0020
* COLLISION_LAYER_7 | $0040
* COLLISION_LAYER_8 | $0080
* COLLISION_LAYER_9 | $0100
* COLLISION_LAYER_10 | $0200
* COLLISION_LAYER_11 | $0400
* COLLISION_LAYER_12 | $0800
* COLLISION_LAYER_13 | $1000
* COLLISION_LAYER_14 | $2000
* COLLISION_LAYER_15 | $4000
* COLLISION_LAYER_16 | $8000
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



