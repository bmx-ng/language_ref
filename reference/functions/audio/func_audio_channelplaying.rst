.. _func_audio_channelplaying:

==============
ChannelPlaying
==============

ChannelPlaying - 

Description
===========

.. code-block:: blitzmax

    ChannelPlaying( channel:TChannel )

Determine whether an audio channel is playing

#ChannelPlaying will return #False if either the channel has been paused using #PauseChannel,
or stopped using #StopChannel.

Parameters
==========

Return Values
=============

#True if @channel is currently playing

Examples
========

.. code-block:: blitzmax

    ' channelplaying.bmx
    
    sound = LoadSound ("shoot.wav")
    
    Input "Hit return to begin channelplaying test, use ctrl-C to exit"
    
    channel=playsound (sound)
    while true
        print "ChannelPlaying(channel)="+ChannelPlaying(channel)
    wend

See Also
========



