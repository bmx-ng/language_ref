.. _func_graphics_max2d_loadimage:

=========
LoadImage
=========

LoadImage - 

Description
===========

.. code-block:: blitzmax

    LoadImage:TImage( url:Object,flags=-1 )

Load an image

@url can be either a string or an existing pixmap.

@flags can be 0, -1 or any combination of:

[ @{Flags value} | @{Effect}

* MASKEDIMAGE | The image is masked with the current mask color.

* FILTEREDIMAGE | The image is smoothed when scaled up to greater than its original
size, when rotated, or when drawn at fractional pixel coordinates.

* MIPMAPPEDIMAGE | The image is smoothed when scaled down to less than its original size.

* DYNAMICIMAGE | The image can be modified using #LockImage or #GrabImage.
]


Note MIPMAPPEDIMAGE images consume extra video memory, so this flag should only be used
when really necessary.

If flags is -1, the auto image flags are used: See #AutoImageFlags.

To combine flags, use the | (boolean OR) operator.

Parameters
==========

Return Values
=============

A new image object

Examples
========

See Also
========



