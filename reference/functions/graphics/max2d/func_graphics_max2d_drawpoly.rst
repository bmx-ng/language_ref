.. _func_graphics_max2d_drawpoly:

========
DrawPoly
========

DrawPoly - 

Description
===========

.. code-block:: blitzmax

    DrawPoly( xy#[] )

Draw a polygon

#DrawPoly draws a polygon with corners defined by an array of x#,y# coordinate pairs.

BlitzMax commands that affect the drawing of polygons include #SetColor, #SetHandle,
#SetScale, #SetRotation, #SetOrigin, #SetViewPort, #SetBlend and #SetAlpha.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' drawpoly.bmx
    
    ' draws a simple triangle using the
    ' DrawPoly command and an array of
    ' floats listed as 3 pairs of x,y
    ' coordinates
    
    Local tri#[]=[0.0,0.0,100.0,100.0,0.0,100.0]
    
    Graphics 640,480
    While Not KeyHit(KEY_ESCAPE)
        Cls
        DrawPoly tri
        Flip
    Wend

See Also
========



