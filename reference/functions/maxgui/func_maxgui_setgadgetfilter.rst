.. _func_maxgui_setgadgetfilter:

===============
SetGadgetFilter
===============

SetGadgetFilter - 

Description
===========

.. code-block:: blitzmax

    SetGadgetFilter( gadget:TGadget,callback(event:TEvent,context:Object),context:Object=Null )

Attaches an event filter function to a MaxGUI gadget.

The filter function supplied is called by the gadget with a #TEvent
and optional user context object. If the function returns zero the event
is filtered and not processed further by the system whereas a non zero
return indicates event processing should proceed as normal.

The TextArea/TextField events currently supported:

[ @{Event ID} | @Description
* EVENT_KEYDOWN | Key pressed. Event data contains keycode.
* EVENT_KEYCHAR | Key character. Event data contains unicode value.
]

Currently only the EVENT_KEYDOWN, EVENT_KEYCHAR events produced by
TextArea and TextField gadgets can be filtered with the SetGadgetFilter
command.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' setgadgetfilter.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Global textarea:TGadget
    
    window=CreateWindow("My Window",30,20,320,240)
    
    textarea=CreateTextArea(0,24,ClientWidth(window),ClientHeight(window)-24,window)
    
    SetGadgetLayout textarea,1,1,1,1
    SetGadgetText textarea,"A textarea gadget that filters out down arrows~nand tab keys."
    ActivateGadget textarea
    
    SetGadgetFilter textarea,filter
    
    Print "KEY_TAB="+KEY_TAB
    
    Function filter(event:TEvent,context:Object)
        Select event.id
            Case EVENT_KEYDOWN
                Print "filtering keydown:"+event.data+","+event.mods
                If event.data=KEY_DOWN Return 0
                If event.data=13 Return 0
            Case EVENT_KEYCHAR
                Print "filtering charkey:"+event.data+","+event.mods
                If event.data=KEY_TAB Return 0
        End Select
        Return 1
    End Function
    
    While WaitEvent()
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
        End Select
    Wend

See Also
========



