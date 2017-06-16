.. _func_graphics_max2d_cls:

===
Cls
===

Cls - 

Description
===========

.. code-block:: blitzmax

    Cls()

Clear graphics buffer

Clears the graphics buffer to the current cls color as determined by #SetClsColor.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' cls.bmx
    
    ' a spinning text message
    ' remove the call to cls to illustrate the
    ' need for clearing the screen every frame
    
    Graphics 640,480
    SetOrigin 320,240
    While Not KeyHit(KEY_ESCAPE)
        Cls 
        SetRotation frame
        DrawText "Press Escape To Exit",0,0
        Flip
        frame:+1
    Wend

See Also
========



