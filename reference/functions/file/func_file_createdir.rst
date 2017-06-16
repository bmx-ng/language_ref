.. _func_file_createdir:

=========
CreateDir
=========

CreateDir - 

Description
===========

.. code-block:: blitzmax

    CreateDir( path$,recurse=False )

Create a directory

If @recurse is true, any required subdirectories are also created.

Parameters
==========

Return Values
=============

True if successful

Examples
========

.. code-block:: blitzmax

    ' createdir.bmx
    
    success=createdir("myfolder")
    if not success runtimeerror "error creating directory"

See Also
========



