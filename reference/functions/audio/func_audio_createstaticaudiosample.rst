.. _func_audio_createstaticaudiosample:

=======================
CreateStaticAudioSample
=======================

CreateStaticAudioSample - 

Description
===========

.. code-block:: blitzmax

    CreateStaticAudioSample:TAudioSample( samples:Byte Ptr,length,hertz,format )

Create an audio sample with existing data

The memory referenced by a static audio sample is not released when the audio sample is
deleted.

See #CreateAudioSample for possile @format values.

Parameters
==========

Return Values
=============

An audio sample object that references an existing block of memory

Examples
========

See Also
========



