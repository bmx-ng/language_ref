.. _func_string_mid:

===
Mid
===

Mid - 

Description
===========

.. code-block:: blitzmax

    Mid$( str$,pos,size=-1 )

Extract substring from a string

The Mid$ command returns a substring of a String.

Given an existing string, a @position from the start of the string and
an optional @size, #Mid creates a new string equal to the section specified.
If no size if given, #Mid returns the characters in the existing string from
@position to the end of the string.

For compatibility with classic BASIC, the @pos parameter is 'one based'.

Parameters
==========

Return Values
=============

A sequence of characters from @str starting at position @pos and of length @size

Examples
========

See Also
========



