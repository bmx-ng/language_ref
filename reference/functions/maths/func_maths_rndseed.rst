.. _func_maths_rndseed:

=======
RndSeed
=======

RndSeed - 

Description
===========

.. code-block:: blitzmax

    RndSeed()

Get random number generator seed
Use in conjunction with SeedRnd, RndSeed allows you to reproduce sequences of random
numbers.

Parameters
==========

Return Values
=============

The current random number generator seed

Examples
========

.. code-block:: blitzmax

    ' RndSeed.bmx and SeedRnd.bmx ( one example for both )
    ' Get/Set random number seed.
    
    SeedRnd MilliSecs()
    
    seed=RndSeed()
    
    Print "Initial seed="+seed
    
    For k=1 To 10
    Print Rand(10)
    Next
    
    Print "Restoring seed"
    
    SeedRnd seed
    
    For k=1 To 10
    Print Rand(10)
    Next

See Also
========



