.. _func_event_addhook:

=======
AddHook
=======

AddHook - 

Description
===========

.. code-block:: blitzmax

    AddHook( id,func:Object( id,data:Object,context:Object ),context:Object=Null,priority=0 )

Add a hook function

Add a hook function to be executed when #RunHooks is called with the specified hook @id.

Parameters
==========

Return Values
=============

A hook object that can be used with the #RemoveHook command.

Examples
========

.. code-block:: blitzmax

    'This function will be automagically called every Flip
    Function MyHook:Object( id,data:Object,context:Object )
        Global count
        
        count:+1
        If count Mod 10=0 Print "Flips="+count
        
    End Function
    
    'Add our hook to the system
    AddHook FlipHook,MyHook
    
    'Some simple graphics
    Graphics 640,480,0
    
    While Not KeyHit( KEY_ESCAPE )
    
        Cls
        DrawText MouseX()+","+MouseY(),0,0
        Flip
    
    Wend

See Also
========



