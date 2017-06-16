.. _func_audio_playsound:

=========
PlaySound
=========

PlaySound - 

Description
===========

.. code-block:: blitzmax

    PlaySound:TChannel( sound:TSound,channel:TChannel=Null )

Play a sound

#PlaySound starts a sound playing through an audio channel.
If no @channel is specified, #PlaySound automatically allocates a channel for you.

Parameters
==========

Return Values
=============

An audio channel object

Examples
========

.. code-block:: blitzmax

    Rem
    Load and Play a small example wav file with looping.
    End Rem
    
    sound=LoadSound("shoot.wav",true)
    PlaySound sound
    
    Input "Press any key to continue"

See Also
========



