.. _func_file_writefile:

=========
WriteFile
=========

WriteFile - 

Description
===========

.. code-block:: blitzmax

    WriteFile:TStream( url:Object )

Open a file for output.

This command is identical to the #WriteStream command.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' writefile.bmx
    
    file=writefile("test.txt")
    
    if not file runtimeerror "failed to open test.txt file" 
    
    writeline file,"hello world"
    
    closestream file

See Also
========



