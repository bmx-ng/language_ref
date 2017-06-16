.. _func_maxgui_setpointer:

==========
SetPointer
==========

SetPointer - 

Description
===========

.. code-block:: blitzmax

    SetPointer(shape)

Sets the mouse cursor.

The shape of the system mouse pointer can be one of the following:

%{Note: Some pointers may not be supported on all platforms.}

[ @Constant | @Description
* POINTER_DEFAULT | Default OS pointer.
* POINTER_ARROW | Arrow pointer.
* POINTER_IBEAM | Typically used when making text selections.
* POINTER_WAIT | Hourglass animation.
* POINTER_CROSS | Typically used for precise drawing.
* POINTER_UPARROW | Typically used for selections.
* POINTER_SIZENWSE | Typically used over sizing handles.
* POINTER_SIZENESW | Typically used over sizing handles.
* POINTER_SIZEWE | Typically used over sizing handles.
* POINTER_SIZENS | Typically used over sizing handles.
* POINTER_SIZEALL | Typically shown when moving an item.
* POINTER_NO | Typically shown when an action is prohibited.
* POINTER_HAND | Typically used for links.
* POINTER_APPSTARTING | Usually shows a pointer and miniature hourglass animation.
* POINTER_HELP | Usually shows an arrow pointer, with an adjacent question mark.
]

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' setpointer.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Local combo:TGadget
    
    window=CreateWindow("SetPointer",40,40,320,240,,WINDOW_TITLEBAR)
    
    CreateLabel "Select a pointer shape:",10,10,200,20,window
    
    combo=CreateComboBox(10,30,200,24,window)
    AddGadgetItem combo,"POINTER_DEFAULT"
    AddGadgetItem combo,"POINTER_ARROW"
    AddGadgetItem combo,"POINTER_IBEAM" 
    AddGadgetItem combo,"POINTER_WAIT" 
    AddGadgetItem combo,"POINTER_CROSS"
    AddGadgetItem combo,"POINTER_UPARROW" 
    AddGadgetItem combo,"POINTER_SIZENWSE" 
    AddGadgetItem combo,"POINTER_SIZENESW" 
    AddGadgetItem combo,"POINTER_SIZEWE" 
    AddGadgetItem combo,"POINTER_SIZENS" 
    AddGadgetItem combo,"POINTER_SIZEALL" 
    AddGadgetItem combo,"POINTER_NO" 
    AddGadgetItem combo,"POINTER_HAND"
    AddGadgetItem combo,"POINTER_APPSTARTING"
    AddGadgetItem combo,"POINTER_HELP"
    
    SelectGadgetItem combo,0
    
    While True
        WaitEvent 
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
            Case EVENT_GADGETACTION
                SetPointer EventData()
        End Select
    Wend

See Also
========



