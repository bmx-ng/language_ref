.. _func_file_loaddir:

=======
LoadDir
=======

LoadDir - 

Description
===========

.. code-block:: blitzmax

    LoadDir$[]( dir$,skip_dots=True )

Load a directory
The @skip_dots parameter, if true, removes the '.' (current) and '..'
(parent) directories from the returned array.

Parameters
==========

Return Values
=============

A string array containing contents of @dir

Examples
========

.. code-block:: blitzmax

    ' loaddir.bmx
    
    ' declare a string array
    
    local files$[]
    
    files=loaddir(currentdir())
    
    for t$=eachin files
        print t    
    next

See Also
========



