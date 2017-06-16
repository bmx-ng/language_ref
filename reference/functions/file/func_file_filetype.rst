.. _func_file_filetype:

========
FileType
========

FileType - 

Description
===========

.. code-block:: blitzmax

    FileType( path$ )

Get file type

Parameters
==========

Return Values
=============

0 if file at @path doesn't exist, FILETYPE_FILE (1) if the file is a plain file or FILETYPE_DIR (2) if the file is a directory

Examples
========

.. code-block:: blitzmax

    ' filetype.bmx
    
    print filetype(".")        'prints 2 for directory type
    print filetype("filetype.bmx")    'prints 1 for file type
    print filetype("notfound.file")    'prints 0 for doesn't exist

See Also
========



