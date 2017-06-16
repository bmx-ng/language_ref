.. _func_file_setfilemode:

===========
SetFileMode
===========

SetFileMode - 

Description
===========

.. code-block:: blitzmax

    SetFileMode( path$,mode )

Set file mode

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' setfilemode.bmx
    
    ' the following makes this source file readonly
    
    writebits=%010010010
    
    ' read the file mode
    
    mode=filemode("setfilemode.bmx")
    
    'mask out the write bits to make readonly
    
    mode=mode & ~writebits
    
    'set the new file mode
    
    setfilemode("setfilemode.bmx",mode)

See Also
========



