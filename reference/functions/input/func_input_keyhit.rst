.. _func_input_keyhit:

======
KeyHit
======

KeyHit - 

Description
===========

.. code-block:: blitzmax

    KeyHit( key )

Check for key hit

The returned value represents the number of the times @key has been hit since the last
call to #KeyHit with the same @key.

See the #{key codes} module for a list of valid key codes.

Parameters
==========

Return Values
=============

Number of times @key has been hit.

Examples
========

.. code-block:: blitzmax

    ' keyhit.bmx
    
    ' the following code draws a circle every time the
    ' program detects the spacebar has been pressed
    ' and exits when it detects the ESCAPE key has
    ' been pressed
    
    graphics 640,480
    while not keyhit(KEY_ESCAPE)
        cls
        if keyhit(KEY_SPACE) drawoval 0,0,640,480
        flip
    wend

See Also
========



