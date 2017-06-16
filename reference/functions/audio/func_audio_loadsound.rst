.. _func_audio_loadsound:

=========
LoadSound
=========

LoadSound - 

Description
===========

.. code-block:: blitzmax

    LoadSound:TSound( url:Object,flags=0 )

Load a sound

@url can be either a string, a stream or a #TAudioSample object.
The returned sound can be played using #PlaySound or #CueSound.

The @flags parameter can be any combination of:

[ @{Flag value} | @Effect
* SOUND_LOOP | The sound should loop when played back.
* SOUND_HARDWARE | The sound should be placed in onboard soundcard memory if possible.
]

To combine flags, use the binary 'or' operator: '|'.

Parameters
==========

Return Values
=============

A sound object

Examples
========

.. code-block:: blitzmax

    Rem
    Load and Play a small example wav file.
    End Rem
    
    sound=LoadSound("shoot.wav")
    PlaySound sound
    
    Input "Press any key to continue"

See Also
========



