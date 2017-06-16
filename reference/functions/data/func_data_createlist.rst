.. _func_data_createlist:

==========
CreateList
==========

CreateList - 

Description
===========

.. code-block:: blitzmax

    CreateList:TList()

Create a linked list

Parameters
==========

Return Values
=============

A new linked list object

Examples
========

.. code-block:: blitzmax

    ' createlist.bmx
    
    ' create a list to hold some objects
    
    list:TList=createlist()
    
    ' add some string objects to the list
    
    listaddlast list,"one"
    listaddlast list,"two"
    listaddlast list,"three"
    
    ' enumerate all the strings in the list
    
    for a$=eachin list
        print a$
    next

See Also
========



