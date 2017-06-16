.. _func_system_requestfile:

===========
RequestFile
===========

RequestFile - 

Description
===========

.. code-block:: blitzmax

    RequestFile$( text$,extensions$="",save_flag=False,initial_path$="" )

Display system file requester.

@text is used as the title of the file requester.

The optional @extensions string can either be a comma separated list of
file extensions or as in the following example groups of extensions
that begin with a "group:" and separated by a semicolon.
@save_flag can be True to create a save-style requester, or False to create a load-style requester.

@initial_path is the initial path for the file requester.

Note that a user interface may not be available when in graphics mode on some platforms.

Parameters
==========

Return Values
=============

The path of the selected file or an empty string if the operation was cancelled.

Examples
========

.. code-block:: blitzmax

    ' requestfile.bmx
    
    filter$="Image Files:png,jpg,bmp
    Text Files:txt
    All Files:*"
    filename$=RequestFile( "Select graphic file to open",filter$ )
    
    Print filename

See Also
========



