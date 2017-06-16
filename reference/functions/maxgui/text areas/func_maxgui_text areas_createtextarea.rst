.. _func_maxgui_text areas_createtextarea:

==============
CreateTextArea
==============

CreateTextArea - 

Description
===========

.. code-block:: blitzmax

    CreateTextArea:TGadget(x,y,w,h,group:TGadget,style=0)

Create a TextArea gadget.

A TextArea gadget is a multiline text editor with commands that allow control
over the contents, style and selection of the text it contains.

A TextArea gadget may have the following optional styles:

[ @Style | @Meaning
* TEXTAREA_WORDWRAP | Long lines of text 'wrap round' onto the next lines.
* TEXTAREA_READONLY | The text cannot be edited by the user.
]

A TextArea gadget can generate the following events:

[ @{Event ID} | @Description
* EVENT_GADGETACTION | The user has modified the text in a TextArea.
* EVENT_GADGETSELECT | The text-cursor has moved or a selection of text is made by the user.
* EVENT_GADGETMENU | The user has right-clicked somewhere in the TextArea.
]

It is also possible to validate any typed input before it reaches the TextArea using
the #SetGadgetFilter command.

See Also: #SetTextAreaText, #AddTextAreaText, #TextAreaText, #TextAreaLen, #LockTextArea,
#UnlockTextArea, #SetTextAreaTabs, #SetGadgetFont, #SetGadgetColor, #TextAreaCursor,
#TextAreaSelLen, #FormatTextAreaText, #SelectTextAreaText, #TextAreaChar and #TextAreaLine.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createtextarea.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Local textarea:TGadget
    
    window=CreateWindow("My Window",130,20,200,200,,15|WINDOW_ACCEPTFILES)
    
    textarea=CreateTextArea(0,0,ClientWidth(window),ClientHeight(window)/2,window)
    SetGadgetLayout textarea,1,1,1,1
    SetGadgetText textarea,"a textarea gadget~none line~nandanother"
    ActivateGadget textarea
    
    SelectTextAreaText textarea,1,1,TEXTAREA_LINES
    
    Print TextAreaCursor(textarea,TEXTAREA_LINES) 
    Print TextAreaSelLen(textarea,TEXTAREA_LINES) 
    
    While WaitEvent()
        Print CurrentEvent.ToString()+" "+EventSourceHandle()
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
            Case EVENT_APPTERMINATE
                End
        End Select
    Wend

See Also
========



