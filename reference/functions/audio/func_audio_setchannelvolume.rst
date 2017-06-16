.. _func_audio_setchannelvolume:

================
SetChannelVolume
================

SetChannelVolume - 

Description
===========

.. code-block:: blitzmax

    SetChannelVolume( channel:TChannel,volume# )

Set playback volume of an audio channel

@volume should be in the range 0 (silent) to 1 (full volume)

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' setchannelvolume.bmx
    
    timer=CreateTimer(20)
    
    sound = LoadSound ("shoot.wav")
    
    For volume#=.1 To 2 Step .05
        WaitTimer timer
        channel=CueSound(sound)
        SetChannelVolume channel,volume
        ResumeChannel channel
    Next

See Also
========



