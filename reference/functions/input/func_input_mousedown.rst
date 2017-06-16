.. _func_input_mousedown:

=========
MouseDown
=========

MouseDown - 

Description
===========

.. code-block:: blitzmax

    MouseDown( button )

Check for mouse button down state

@button should be 1 for the left mouse button, 2 for the right mouse button or 3 for the
middle mouse button.

Parameters
==========

Return Values
=============

#True if @button is currently down

Examples
========

.. code-block:: blitzmax

    ' mousedown.bmx
    
    graphics 640,480
    
    while not keyhit(KEY_ESCAPE)
        cls
        if mousedown(1) drawrect 0,0,200,200
        if mousedown(2) drawrect 200,0,200,200
        if mousedown(3) drawrect 400,0,200,200
        flip
    wend

See Also
========



