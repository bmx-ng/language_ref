.. _func_input_keydown:

=======
KeyDown
=======

KeyDown - 

Description
===========

.. code-block:: blitzmax

    KeyDown( key )

Check for key state

See the #{key codes} module for a list of valid keycodes.

Parameters
==========

Return Values
=============

#True if @key is currently down

Examples
========

.. code-block:: blitzmax

    ' keydown.bmx
    
    ' the following code draws a circle if the
    ' program detects the spacebar is pressed
    ' and exits when it detects the ESCAPE key has
    ' been pressed
    
    Graphics 640,480
    While Not KeyHit(KEY_ESCAPE)
        Cls
        If KeyDown(KEY_SPACE) DrawOval 0,0,640,480
        Flip
    Wend

See Also
========



