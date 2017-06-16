.. _func_system_confirm:

=======
Confirm
=======

Confirm - 

Description
===========

.. code-block:: blitzmax

    Confirm( text$,serious=False )

Request user confirmation.

#Confirm activates a simple user interface element requesting the user to select between
YES and NO options. If the user selects YES, then #Confirm returns True. Otherwise,
False is returned.

Note that a user interface may not be available when in graphics mode on some platforms.

Parameters
==========

Return Values
=============

True or False depending on the user's selection

Examples
========

.. code-block:: blitzmax

    ' confirm.bmx
    
    result=Confirm("Are you sure?")
    
    print result

See Also
========



