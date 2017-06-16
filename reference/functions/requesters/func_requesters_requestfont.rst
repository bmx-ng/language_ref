.. _func_requesters_requestfont:

===========
RequestFont
===========

RequestFont - 

Description
===========

.. code-block:: blitzmax

    RequestFont:TGuiFont(font:TGuiFont=Null)

Prompts the user to select a system font.

Prompts the user for a font and returns an object that can be used with the #SetGadgetFont command.

See Also: #LoadGuiFont, #LookupGuiFont, #FontName, #FontSize and #FontStyle

Parameters
==========

Return Values
=============

A @TGuiFont object, or #Null if no font was selected.

Examples
========

.. code-block:: blitzmax

    ' requestfont.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Local button:TGadget
    Local label:TGadget
    Local font:TGuiFont
    
    window=CreateWindow("RequestFont",30,20,200,250)
    label=CreateLabel("font example",4,4,192,132,window)
    button=CreateButton("Select Font",4,140,100,20,window)
    
    While WaitEvent()
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
            Case EVENT_GADGETACTION
                font=RequestFont(font)
                If font
                    SetGadgetFont label,font
                    SetGadgetText label,FontName(font)+":"+FontSize(font)
                EndIf
        End Select
    Wend

See Also
========



