.. _func_system_gcsuspend:

=========
GCSuspend
=========

GCSuspend - 

Description
===========

.. code-block:: blitzmax

    GCSuspend()

Suspend garbage collector

#GCSuspend temporarily suspends the garbage collector. No garbage
collection will be performed following a call to #GCSuspend.<br>
<br>
Use #GCResume to resume the garbage collector. Note that #GCSuspend
and #GCResume 'nest', meaning that each call to #GCSuspend must be
matched by a call to #GCResume.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



