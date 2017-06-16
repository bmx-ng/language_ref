.. _func_system_requestdir:

==========
RequestDir
==========

RequestDir - 

Description
===========

.. code-block:: blitzmax

    RequestDir$( text$,initial_path$="" )

Display system folder requester.

@text is used as the title of the file requester.

@initial_path is the initial path for the folder requester.

Note that a user interface may not be available when in graphics mode on some platforms.

Parameters
==========

Return Values
=============

The path of the selected folder or an empty string if the operation was cancelled.

Examples
========

.. code-block:: blitzmax

    ' requestdir.bmx
    
    path$=RequestDir("Select a Folder",CurrentDir())
    
    Print "directory selected was "+path

See Also
========



