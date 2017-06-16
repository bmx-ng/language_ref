.. _func_graphics_graphicsmodes:

=============
GraphicsModes
=============

GraphicsModes - 

Description
===========

.. code-block:: blitzmax

    GraphicsModes:TGraphicsMode[]()

Get graphics modes available under the current graphics driver

A TGraphicsMode object contains the following fields: @width, @height, @depth and @hertz

Parameters
==========

Return Values
=============

An array of TGraphicsMode objects

Examples
========

.. code-block:: blitzmax

    Print "Available graphics modes:"
    
    For mode:TGraphicsMode=EachIn GraphicsModes()
    
        Print mode.width+","+mode.height+","+mode.depth+","+mode.hertz
    
    Next

See Also
========



