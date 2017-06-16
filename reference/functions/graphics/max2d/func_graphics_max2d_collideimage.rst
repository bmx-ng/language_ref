.. _func_graphics_max2d_collideimage:

============
CollideImage
============

CollideImage - 

Description
===========

.. code-block:: blitzmax

    CollideImage:Object[](image:TImage,x,y,frame,collidemask%,writemask%,id:Object=Null)

Pixel accurate collision testing between transformed Images.

The @collidemask specifies any layers to test for collision with.

The @writemask specifies which if any collision layers the @image is added to in it's currently transformed state.

The id specifies an object to be returned to future #CollideImage calls when collisions occur.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    Strict
    
    Local rot,x,y
    
    Graphics 640,480
    
    AutoMidHandle True    'image will rotate around it's center
    
    Local image:TImage=LoadImage("bullet.png")
    
    While Not KeyHit(KEY_ESCAPE)
        Cls
        ResetCollisions
    
    ' draw the first image at 5 times the size and on an arbitrary angle
        
        SetScale 5,5
        SetRotation 125
    
        DrawImage image,200,200
    
    ' add the first image to the first collision layer at same postion, rotation 
    ' and scale as it has just been drawn
    
        CollideImage image,200,200,0,0,1
    
    ' move the other image relative to the mouse and rotate it continuously
    
        x=MouseX()
        y=MouseY()-20
        rot:+1
    
        SetRotation rot
        DrawImage image,x,y
    
    ' test the image at it's current rotation, scale and position with images
    ' that have been added to the first collision layer
    
        If CollideImage(image,x,y,0,1,0)
    
    ' reset scale and rotation states so our text is drawn correctly        
    
            SetScale 1,1
            SetRotation 0
            DrawText "COLLISION!",20,20
    
        EndIf
    
        Flip
    Wend

See Also
========



