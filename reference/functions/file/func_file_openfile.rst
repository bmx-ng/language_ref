.. _func_file_openfile:

========
OpenFile
========

OpenFile - 

Description
===========

.. code-block:: blitzmax

    OpenFile:TStream( url:Object,readable=True,writeable=True )

Open a file for input and/or output.

This command is similar to the #OpenStream command but will attempt
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

    ' openfile.bmx
    
    ' the following prints the contents of this source file 
    
    file=openfile("openfile.bmx")
    
    if not file runtimeerror "could not open file openfile.bmx"
    
    while not eof(file)
        print readline(file)
    wend
    closestream file

See Also
========



