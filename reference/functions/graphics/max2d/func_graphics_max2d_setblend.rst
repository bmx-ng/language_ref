.. _func_graphics_max2d_setblend:

========
SetBlend
========

SetBlend - 

Description
===========

.. code-block:: blitzmax

    SetBlend( blend )

Set current blend mode

SetBlend controls how pixels are combined with existing pixels in the back buffer when drawing
commands are used in BlitzMax.

@blend should be one of:

[ @{Blend mode} | @Effect
* MASKBLEND | Pixels are drawn only if their alpha component is greater than .5
* SOLIDBLEND | Pixels overwrite existing backbuffer pixels
* ALPHABLEND | Pixels are alpha blended with existing backbuffer pixels
* LIGHTBLEND | Pixel colors are added to backbuffer pixel colors, giving a 'lighting' effect
* SHADEBLEND | Pixel colors are multiplied with backbuffer pixel colors, giving a 'shading' effect
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



