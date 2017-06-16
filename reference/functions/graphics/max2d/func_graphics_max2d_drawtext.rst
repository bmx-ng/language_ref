.. _func_graphics_max2d_drawtext:

========
DrawText
========

DrawText - 

Description
===========

.. code-block:: blitzmax

    DrawText( t$,x#,y# )

Draw text

#DrawText prints strings at position @x,@y of the graphics display using
the current image font specified by the #SetImageFont command.

Other commands that affect #DrawText include #SetColor, #SetHandle,
#SetScale, #SetRotation, #SetOrigin, #SetViewPort, #SetBlend and #SetAlpha.

It is recomended that the blend mode be set to ALPHABLEND using the #SetBlend
command for non jagged antialiased text. Text that will be drawn at a smaller
size using the #SetScale command should use fonts loaded with the SMOOTHFONT
style to benefit from mip-mapped filtering, see #LoadImageFont for more information.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' drawtext.bmx
    
    ' scrolls a large text string across the screen by decrementing the tickerx variable
    
    Graphics 640,480
    
    Local tickerx#=640
    
    text$="Yo to all the Apple, Windows and Linux BlitzMax programmers in the house! "
    text:+"Game development is the most fun, most advanced and definitely most cool "
    text:+"software programming there is!"
    
    While Not KeyHit(KEY_ESCAPE)
        Cls
        DrawText "Scrolling Text Demo",0,0
        DrawText text,tickerx#,400
        tickerx=tickerx-1
        If tickerx<-TextWidth(text) tickerx=640
        Flip    
    Wend
    
    End

See Also
========



