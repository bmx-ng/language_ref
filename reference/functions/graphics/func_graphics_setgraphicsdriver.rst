.. _func_graphics_setgraphicsdriver:

=================
SetGraphicsDriver
=================

SetGraphicsDriver - 

Description
===========

.. code-block:: blitzmax

    SetGraphicsDriver( driver:TGraphicsDriver,defaultFlags=GRAPHICS_BACKBUFFER )

Set current graphics driver

The current graphics driver determines what kind of graphics are created when you use
the #CreateGraphics or #Graphics functions, as well as the graphics modes available.

The #GLGraphicsDriver, #GLMax2DDriver and #D3D7Max2DDriver functions can all be used to
obtain a graphics driver.

The @defaultFlags parameter allows you to specify graphics flags that will be applied to any
graphics created with #CreateGraphics or #Graphics.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    SetGraphicsDriver GLMax2DDriver()
    
    Graphics 640,480
    DrawText "OpenGL Max2D Graphics! Hit any key (next to the whatever key)...",0,0
    Flip
    WaitKey
    EndGraphics
    
    SetGraphicsDriver GLGraphicsDriver()
    
    Graphics 640,480
    glClear GL_COLOR_BUFFER_BIT
    GLDrawText "'Raw' OpenGL Graphics! Hit any key...",0,0
    Flip
    WaitKey

See Also
========



