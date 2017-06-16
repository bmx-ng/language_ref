.. _func_audio_cuesound:

========
CueSound
========

CueSound - 

Description
===========

.. code-block:: blitzmax

    CueSound:TChannel( sound:TSound,channel:TChannel=Null )

Cue a sound

Prepares a sound for playback through an audio channel.
To actually start the sound, you must use #ResumeChannel.
If no @channel is specified, #CueSound automatically allocates a channel for you.

#CueSound allows you to setup various audio channel states such as volume, pan, depth
and rate before a sound actually starts playing.

Parameters
==========

Return Values
=============

An audio channel object

Examples
========

.. code-block:: blitzmax

    Rem
    CueSound example
    End Rem
    
    sound=LoadSound("shoot.wav")
    channel=CueSound(sound)
    
    Input "Press return key to play cued sound"
    
    ResumeChannel channel
    
    Input "Press return key to quit"

See Also
========



