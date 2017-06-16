.. _func_file_stripslash:

==========
StripSlash
==========

StripSlash - 

Description
===========

.. code-block:: blitzmax

    StripSlash$( path$ )

Strip trailing slash from a file path

#StripSlash will not remove the trailing slash from a 'root' path. For example, "/"
or (on Win32 only) "C:/".

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' stripslash.bmx
    
    print stripslash("mypath/")    'prints mypath

See Also
========



