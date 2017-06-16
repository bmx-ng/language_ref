.. _func_graphics_flip:

====
Flip
====

Flip - 

Description
===========

.. code-block:: blitzmax

    Flip( sync=-1 )

Flip current graphics object

#Flip swap the front and back buffers of the current graphics objects.

If @sync is 0, then the flip occurs as soon as possible. If @sync is 1, then the flip occurs
on the next vertical blank.

If @sync is -1 and the current graphics object was created with the #Graphics command,
then flips will occur at the graphics object's refresh rate regardless of whether or not the
graphics hardware supports such a refresh rate.

If @sync is -1 and the current graphics object was NOT created with the #Graphics command,
then the flip will occur on the next vertical blank.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



