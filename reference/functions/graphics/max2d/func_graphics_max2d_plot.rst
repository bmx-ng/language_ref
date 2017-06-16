.. _func_graphics_max2d_plot:

====
Plot
====

Plot - 

Description
===========

.. code-block:: blitzmax

    Plot( x#,y# )

Plot a pixel

Sets the color of a single pixel on the back buffer to the current drawing color
defined with the #SetColor command. Other commands that affect the operation of
#Plot include #SetOrigin, #SetViewPort, #SetBlend and #SetAlpha.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' plot.bmx
    
    ' plots a cosine graph
    ' scrolls along the graph using an incrementing frame variable 
    
    Graphics 640,480
    
    While Not KeyHit(KEY_ESCAPE)
        Cls
        For x=0 To 640
            theta=x+frame
            y=240-Cos(theta)*240
            Plot x,y
        Next
        frame=frame+1
        Flip
    Wend

See Also
========



