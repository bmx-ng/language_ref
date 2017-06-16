.. _func_file_readdir:

=======
ReadDir
=======

ReadDir - 

Description
===========

.. code-block:: blitzmax

    ReadDir( path$ )

Open a directory

Parameters
==========

Return Values
=============

An integer directory handle, or 0 if the directory does not exist

Examples
========

.. code-block:: blitzmax

    ' readdir.bmx
    
    dir=ReadDir(CurrentDir())
    
    If Not dir RuntimeError "failed to read current directory"
    
    Repeat
        t$=NextFile( dir )
        If t="" Exit
        If t="." Or t=".." Continue
        Print t    
    Forever
    
    CloseDir dir

See Also
========



