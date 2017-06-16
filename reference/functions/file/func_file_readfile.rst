.. _func_file_readfile:

========
ReadFile
========

ReadFile - 

Description
===========

.. code-block:: blitzmax

    ReadFile:TStream( url:Object )

Open a file for input.

This command is similar to the #ReadStream command but will attempt
to cache the contents of the file to ensure serial streams such as
http: based url's are seekable. Use the #CloseStream command when
finished reading and or writing to a Stream returned by #OpenFile.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' readfile.bmx
    
    ' the following prints the contents of this source file 
    
    file=readfile("readfile.bmx")
    
    if not file runtimeerror "could not open file openfile.bmx"
    
    while not eof(file)
        print readline(file)
    wend
    
    closestream file

See Also
========



