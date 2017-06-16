.. _func_maths_rand:

====
Rand
====

Rand - 

Description
===========

.. code-block:: blitzmax

    Rand( min_value,max_value=1 )

Generate random integer

The optional parameter allows you to use #Rand in 2 ways:

[ @Format | @Result
* &Rand(x) | Random integer in the range 1 to x (inclusive)
* &Rand(x,y) | Random integer in the range x to y (inclusive)
]

Parameters
==========

Return Values
=============

A random integer in the range min (inclusive) to max (inclusive)

Examples
========

.. code-block:: blitzmax

    ' Rand.bmx
    ' Toss a pair of dice. Result is in the range 1+1 to 6+6.
    ' Count how many times each result appears.
    
    Local count[13]
    
    For n = 1 To 3600
        toss = Rand(1,6) + Rand(1,6)
        count[toss] :+ 1
    Next
    
    For toss = 2 To 12
        Print LSet(toss, 5)+count[toss]
    Next

See Also
========



