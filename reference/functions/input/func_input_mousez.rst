.. _func_input_mousez:

======
MouseZ
======

MouseZ - 

Description
===========

.. code-block:: blitzmax

    MouseZ()

Get mouse wheel

The mouse wheel value increments when the mouse wheel is rolled 'away' from the user, and
decrements when the mouse wheel is rolled 'towards' the user.

Parameters
==========

Return Values
=============

Mouse wheel value

Examples
========

.. code-block:: blitzmax

    ' mousez.bmx
    
    ' prints mousez() the mousewheel position
    
    Graphics 640,480
    While Not keyhit(KEY_ESCAPE)
        cls
        drawtext "MouseZ()="+MouseZ(),0,0
        flip
    Wend

See Also
========



