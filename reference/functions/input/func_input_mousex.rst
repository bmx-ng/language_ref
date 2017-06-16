.. _func_input_mousex:

======
MouseX
======

MouseX - 

Description
===========

.. code-block:: blitzmax

    MouseX()

Get mouse x location

The returned value is relative to the left of the screen.

Parameters
==========

Return Values
=============

Mouse x axis location

Examples
========

.. code-block:: blitzmax

    ' mousex.bmx
    
    ' the following tracks the position of the mouse
    
    graphics 640,480
    while not keyhit(KEY_ESCAPE)
        cls
        drawoval mousex()-10,mousey()-10,20,20
        flip
    wend

See Also
========



