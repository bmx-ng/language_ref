.. _func_graphics_max2d_drawline:

========
DrawLine
========

DrawLine - 

Description
===========

.. code-block:: blitzmax

    DrawLine( x#,y#,x2#,y2#,draw_last_pixel=True )

Draw a line

#DrawLine draws a line from @x, @y to @x2, @y2 with the current drawing color.

BlitzMax commands that affect the drawing of lines include #SetLineWidth, #SetColor, #SetHandle,
#SetScale, #SetRotation, #SetOrigin, #SetViewPort, #SetBlend and #SetAlpha.
The optional @draw_last_pixel parameter can be used to control whether the last pixel of the line is drawn or not.
Not drawing the last pixel can be useful if you are using certain blending modes.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' drawline.bmx
    
    ' draws a cross hair at the mouse position using DrawLine
    
    Graphics 640,480
    
    HideMouse 
    
    While Not KeyHit(KEY_ESCAPE)
        Cls
        x=MouseX()
        y=MouseY()
        DrawLine 320,240,x,y
        DrawLine x-2,y,x-10,y
        DrawLine x+2,y,x+10,y
        DrawLine x,y-2,x,y-10
        DrawLine x,y+2,x,y+10
        Flip
    Wend

See Also
========



