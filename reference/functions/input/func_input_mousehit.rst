.. _func_input_mousehit:

========
MouseHit
========

MouseHit - 

Description
===========

.. code-block:: blitzmax

    MouseHit( button )

Check for mouse button click

The returned value represents the number of the times @button has been clicked since the
last call to #MouseHit with the same @button.

@button should be 1 for the left mouse button, 2 for the right mouse button or 3 for the
middle mouse button.

Parameters
==========

Return Values
=============

Number of times @button has been clicked.

Examples
========

.. code-block:: blitzmax

    ' mousehit.bmx
    
    graphics 640,480
    
    while not keyhit(KEY_ESCAPE)
        cls
        if mousehit(1) drawrect 0,0,200,200
        if mousehit(2) drawrect 200,0,200,200
        if mousehit(3) drawrect 400,0,200,200
        flip
    wend

See Also
========



