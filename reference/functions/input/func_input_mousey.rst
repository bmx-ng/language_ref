.. _func_input_mousey:

======
MouseY
======

MouseY - 

Description
===========

.. code-block:: blitzmax

    MouseY()

Get mouse y location

The returned value is relative to the top of the screen.

Parameters
==========

Return Values
=============

Mouse y axis location

Examples
========

.. code-block:: blitzmax

    ' mousey.bmx
    
    ' the following tracks the position of the mouse
    
    graphics 640,480
    while not keyhit(KEY_ESCAPE)
        cls
        drawrect mousex()-10,mousey()-10,20,20
        flip
    wend

See Also
========



