.. _func_audio_setchannelpan:

=============
SetChannelPan
=============

SetChannelPan - 

Description
===========

.. code-block:: blitzmax

    SetChannelPan( channel:TChannel,pan# )

Set stereo balance of an audio channel

@pan should be in the range -1 (left) to 1 (right)

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' setchannelpan.bmx
    
    Graphics 640, 480
    
    channel = AllocChannel ()
    sound = LoadSound ("shoot.wav") ' Use a short sample...
    
    Repeat
        If MouseHit(1) PlaySound sound,channel
        
        pan# = MouseX () / (GraphicsWidth () / 2.0) - 1
        vol# = 1 - MouseY () / 480.0
        SetChannelPan channel, pan
        SetChannelVolume channel, vol*2
    
        Cls
        DrawText "Click to play...", 240, 200
        DrawText "Pan   : " + pan, 240, 220
        DrawText "Volume: " + vol, 240, 240
    
        Flip
    Until KeyHit (KEY_ESCAPE)
    
    End

See Also
========



