.. _func_streams_writestream:

===========
WriteStream
===========

WriteStream - 

Description
===========

.. code-block:: blitzmax

    WriteStream:TStream( url:Object )

Open a stream for writing
All streams created by #OpenStream, #ReadStream or #WriteStream should eventually
be closed using #CloseStream.

Parameters
==========

Return Values
=============

A stream object

Examples
========

.. code-block:: blitzmax

    ' writestream.bmx
    
    ' opens a write stream to the file mygame.ini and
    ' outputs a simple text file using WriteLine
    
    out=WriteStream("mygame.ini")
    
    if not out RuntimeError "Failed to open a WriteStream to file mygame.ini"
    
    WriteLine out,"[display]"
    WriteLine out,"width=800"
    WriteLine out,"height=600"
    WriteLine out,"depth=32"
    WriteLine out,""
    WriteLine out,"[highscores]"
    WriteLine out,"AXE=1000"
    WriteLine out,"HAL=950"
    WriteLine out,"MAK=920"
    
    CloseStream out
    
    print "File mygame.ini created, bytes="+FileSize("mygame.ini")

See Also
========



