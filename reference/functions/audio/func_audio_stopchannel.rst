.. _func_audio_stopchannel:

===========
StopChannel
===========

StopChannel - 

Description
===========

.. code-block:: blitzmax

    StopChannel( channel:TChannel )

Stop an audio channel

Shuts down an audio channel. Further commands using this channel will have no effect.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    Rem
    StopChannel example
    End Rem
    
    sound=LoadSound("shoot.wav",true)
    channel=PlaySound(sound)
    
    print "channel="+channel
    
    Input "Press return key to stop sound"
    
    StopChannel channel
    
    Input "Press return key to quit"

See Also
========



