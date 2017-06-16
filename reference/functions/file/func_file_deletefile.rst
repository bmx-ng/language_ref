.. _func_file_deletefile:

==========
DeleteFile
==========

DeleteFile - 

Description
===========

.. code-block:: blitzmax

    DeleteFile( path$ )

Delete a file

Parameters
==========

Return Values
=============

True if successful

Examples
========

.. code-block:: blitzmax

    ' deletefile.bmx
    
    success=deletefile("myfile")
    if not success runtimeerror "error deleting file"

See Also
========



