.. _func_audio_allocchannel:

============
AllocChannel
============

AllocChannel - 

Description
===========

.. code-block:: blitzmax

    AllocChannel:TChannel()

Allocate audio channel

Allocates an audio channel for use with #PlaySound and #CueSound.
Once you are finished with an audio channel, you should use #StopChannel.

Parameters
==========

Return Values
=============

An audio channel object

Examples
========

.. code-block:: blitzmax

    'AllocChannel.bmx
    
    timer=createtimer(20)
    
    sound=LoadSound ("shoot.wav")
    channel=AllocChannel()
    
    for i=1 to 20
        waittimer timer
        playsound sound,channel
    next

See Also
========



