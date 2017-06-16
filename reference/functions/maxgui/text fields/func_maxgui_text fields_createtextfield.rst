.. _func_maxgui_text fields_createtextfield:

===============
CreateTextField
===============

CreateTextField - 

Description
===========

.. code-block:: blitzmax

    CreateTextField:TGadget(x,y,w,h,group:TGadget,style=0)

Create a TextField gadget.
A TextField is a single line text entry gadget and currently has only one style flag:

[ @Flags | @Meaning
* TEXTFIELD_PASSWORD | Masks characters being typed as a string as asterisks.
]

Irrespective of the flag used, the TextField gadget will emit the following event(s):

[ @{Event ID} | @Description
* EVENT_GADGETACTION | The user has edited the text in the TextField.
]

It is also possible to validate any typed input before it reaches the TextArea using
the #SetGadgetFilter command.

See Also: #GadgetText, #SetGadgetText, #SetGadgetFilter.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createtextfield.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Local textfield:TGadget
    Local button:TGadget
    
    window=CreateWindow("My Window",30,20,320,200)
    
    textfield=CreateTextField(4,4,120,22,window)
    SetGadgetText( textfield,"A textfield gadget" )
    
    ' we need an OK button to catch return key
    
    button=CreateButton("OK",130,4,80,24,window,BUTTON_OK)
    
    ActivateGadget textfield
    
    While WaitEvent()
        Print CurrentEvent.ToString()
        Select EventID()
        Case EVENT_GADGETACTION
            Select EventSource()
                Case textfield
                    Print "textfield updated"
                Case button
                    Print "return key / OK button pressed"
            End Select
        Case EVENT_WINDOWCLOSE
            End
        End Select
    Wend

See Also
========



