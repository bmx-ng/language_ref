.. _func_graphics_max2d_createimage:

===========
CreateImage
===========

CreateImage - 

Description
===========

.. code-block:: blitzmax

    CreateImage:TImage( width,height,frames=1,flags=-1 )

Create an empty image

#CreateImage creates an 'empty' image, which should be initialized using either #GrabImage or #LockImage
before being drawn.

Please refer to #LoadImage for valid @flags values. The @flags value is always combined with DYNAMICIMAGE.

Parameters
==========

Return Values
=============

A new image object

Examples
========

.. code-block:: blitzmax

    ' createimage.bmx
    
    ' creates a 256x1 image with a black to blue color gradient
    
    Const ALPHABITS=$ff000000
    
    Graphics 640,480,32
    
    image=CreateImage(256,1)
    map=LockImage(image)
    For i=0 To 255
        WritePixel(map,i,0,ALPHABITS|i)
    Next
    UnlockImage(image)
    
    DrawImageRect image,0,0,640,480
    DrawText "Blue Color Gradient",0,0
    
    Flip
    
    WaitKey

See Also
========



