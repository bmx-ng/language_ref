.. _func_streams_savetext:

========
SaveText
========

SaveText - 

Description
===========

.. code-block:: blitzmax

    SaveText( str$,url:Object )

Save text to a stream

#SaveText saves the characters in @str to @url.

If @str contains any characters with a character code greater than 255,
then @str is saved in UTF16 format. Otherwise, @str is saved in LATIN1 format.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



