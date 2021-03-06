.. _func_file_filemode:

========
FileMode
========

FileMode - 

Description
===========

.. code-block:: blitzmax

    FileMode( path$ )

Get file mode

Parameters
==========

Return Values
=============

file mode flags

Examples
========

.. code-block:: blitzmax

    ' filemode.bmx
    
    ' the following function converts the file mode to 
    ' the standard unix permission bits string
    
    Function Permissions$(mode)
        local    testbit,pos
        local    p$="rwxrwxrwx"
        testbit=%100000000
        pos=1
        while (testbit)
            if mode & testbit res$:+mid$(p$,pos,1) else res$:+"-"
            testbit=testbit shr 1
            pos:+1    
        wend
        return res
    End Function
    
    print Permissions$(filemode("filemode.bmx"))

See Also
========



