.. _func_maths_rnd:

===
Rnd
===

Rnd - 

Description
===========

.. code-block:: blitzmax

    Rnd!( min_value!=1,max_value!=0 )

Generate random double

The optional parameters allow you to use Rnd in 3 ways:

[ @Format | @Result
* &Rnd() | Random double in the range 0 (inclusive) to 1 (exclusive)
* &Rnd(_x_) | Random double in the range 0 (inclusive) to n (exclusive)
* &Rnd(_x,y_) | Random double in the range x (inclusive) to y (exclusive)
]

Parameters
==========

Return Values
=============

A random double in the range min (inclusive) to max (exclusive)

Examples
========

.. code-block:: blitzmax

    ' Rnd.bmx
    ' Use Rnd() to estimate area inside the unit circle x^2 + y^2 = 1.
    
    totalpoints = 1000000
    
    For n = 1 to totalpoints
        x! = Rnd( -1.0, 1.0 )               ' Generate random point in 2 by 2 square.
        y! = Rnd( -1.0, 1.0 )
    
        If x*x + y*y < 1.0 Then inpoints :+ 1     ' point is inside the circle
    Next
    
    ' Note: Ratio of areas circle/square is exactly Pi/4.
    
    Print "Estimated area = " + ( 4.0 * Double(inpoints)/Double(totalpoints) )
    Print
    Print "    Exact area = " + Pi     '  4 * Pi/4, compare with estimate
    
    Input 
     End

See Also
========



