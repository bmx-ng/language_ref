.. _func_system_proceed:

=======
Proceed
=======

Proceed - 

Description
===========

.. code-block:: blitzmax

    Proceed( text$,serious=False )

Request user confirmation or cancellation.

#Proceed activates a simple user interface element requesting the user to select between
YES, NO and CANCEL options. If the user selects YES, then #Proceed return 1. If the user
selects NO, then #Proceed returns 0. Otherwise, #Proceed returns -1.

Note that a user interface may not be available when in graphics mode on some platforms.

Parameters
==========

Return Values
=============

1, 0 or -1 depending on the user's selection

Examples
========

.. code-block:: blitzmax

    ' proceed.bmx
    
    result=Proceed("Are you sure you want to continue?")
    
    print result

See Also
========



