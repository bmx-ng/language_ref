.. _func_audio_setchannelrate:

==============
SetChannelRate
==============

SetChannelRate - 

Description
===========

.. code-block:: blitzmax

    SetChannelRate( channel:TChannel,rate# )

Set playback rate of an audio channel

@rate is a multiplier used to modify the audio channel's frequency.
For example, a rate of .5 will cause the audio channel
to play at half speed (ie: an octave down) while a rate of 2 will
cause the audio channel to play at double speed (ie: an octave up).

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' setchannelrate.bmx
    
    timer=CreateTimer(20)
    
    sound = LoadSound ("shoot.wav",True)
    channel=CueSound(sound)
    ResumeChannel channel
    
    For rate#=1.0 To 4 Step 0.01
        WaitTimer timer
        SetChannelRate channel,rate
    Next

See Also
========



