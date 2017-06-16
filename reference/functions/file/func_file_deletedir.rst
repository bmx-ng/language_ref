.. _func_file_deletedir:

=========
DeleteDir
=========

DeleteDir - 

Description
===========

.. code-block:: blitzmax

    DeleteDir( path$,recurse=False )

Delete a directory
Set @recurse to true to delete all subdirectories and files recursively -
but be careful!

Parameters
==========

Return Values
=============

True if successful

Examples
========

.. code-block:: blitzmax

    ' deletedir.bmx
    
    success=deletedir("myfolder")
    if not success runtimeerror "error deleting directory"

See Also
========



