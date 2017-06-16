.. _func_audio_createaudiosample:

=================
CreateAudioSample
=================

CreateAudioSample - 

Description
===========

.. code-block:: blitzmax

    CreateAudioSample:TAudioSample( length,hertz,format )

Create an audio sample

@length is the number of samples to allocate for the sample. @hertz is the frequency in samples per second (hz)
the audio sample will be played. @format should be one of:

[ @Format | @Description

* &SF_MONO8 | Mono unsigned 8 bit

* &SF_MONO16LE | Mono signed 16 bit little endian

* &SF_MONO16BE | Mono signed 16 bit big endian

* &SF_STEREO8 | Stereo unsigned 8 bit

* &SF_STEREO16LE | Stereo signed 16 bit little endian

* &SF_STEREO16BE | Stereo signed 16 bit big endian
]

Parameters
==========

Return Values
=============

An audio sample object

Examples
========

.. code-block:: blitzmax

    ' createaudiosample.bmx
    
    Local sample:TAudioSample=CreateAudioSample( 32,11025,SF_MONO8 )
    
    For Local k=0 Until 32
            sample.samples[k]=Sin(k*360/32)*127.5+127.5
    Next
    
    Local sound:TSound=LoadSound( sample,True )
    
    PlaySound(sound)
    
    Input

See Also
========



