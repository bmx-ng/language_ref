.. _func_graphics_max2d_grabimage:

=========
GrabImage
=========

GrabImage - 

Description
===========

.. code-block:: blitzmax

    GrabImage( image:TImage,x,y,frame=0 )

Grab an image from the back buffer

Copies pixels from the back buffer to an image frame.

Only images created with the DYNAMICIMAGE flag can be grabbed.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' grabimage.bmx
    
    ' draws a small graphic then uses grabimage to make an image
    
    ' as mask color and cls color both default to black a mask is 
    ' created for the grabbed where any pixels unset on the backbuffer
    ' become transparent in the grabbed image
    
    Graphics 800,600,0'640,480,32
    
    Cls
    
    DrawLine 0,0,32,32
    DrawLine 32,0,0,32
    DrawOval 0,0,32,32
    
    Local image=CreateImage(640,480,1,DYNAMICIMAGE|MASKEDIMAGE)
    
    GrabImage image,0,0
    
    Cls
    For i=1 To 100
        DrawImage image,Rnd(640),Rnd(480)
    Next
    Flip
    
    GrabImage image,0,0
    Cls
    For i=1 To 100
        DrawImage image,Rnd(640),Rnd(480)
    Next
    Flip
    
    
    WaitKey

See Also
========



