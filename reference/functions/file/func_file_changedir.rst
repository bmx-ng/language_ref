.. _func_file_changedir:

=========
ChangeDir
=========

ChangeDir - 

Description
===========

.. code-block:: blitzmax

    ChangeDir( path$ )

Change current directory

Parameters
==========

Return Values
=============

True if successful

Examples
========

.. code-block:: blitzmax

    ' changedir.bmx
    
    print "CurrentDir()="+currentdir()
    
    ' change current folder to the parent folder
    
    changedir ".."
    
    ' print new CurrentDir()
    
    print "CurrentDir()="+currentdir()

See Also
========



