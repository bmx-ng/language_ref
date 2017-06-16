.. _func_maxgui_labels_createlabel:

===========
CreateLabel
===========

CreateLabel - 

Description
===========

.. code-block:: blitzmax

    CreateLabel:TGadget(name$,x,y,w,h,group:TGadget,style=LABEL_LEFT)

Create a Label gadget.

A Label gadget is used to place static text or frames in a MaxGUI user interface. They do not
generate any events.

Labels support these optional styles:

[ @Style | @Meaning
* LABEL_FRAME | The label has a simple border.
* LABEL_SUNKENFRAME | The label has a sunken border.
* LABEL_SEPARATOR | The label is an etched box with no text useful for drawing separators.
* LABEL_LEFT | The label's text is left-aligned. This is the default.
* LABEL_CENTER | The label's text is center-aligned.
* LABEL_RIGHT | The label's text is right-aligned.
]

See Also: #SetGadgetText, #SetGadgetTextColor, #SetGadgetFont and #SetGadgetColor.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createlabel.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    
    window=CreateWindow("My Window",30,20,320,480)
    
    CreateLabel("A plain label",10,10,280,52,window)
    CreateLabel("A label with LABEL_FRAME",10,80,280,60,window,LABEL_FRAME)
    CreateLabel("A label with LABEL_SUNKENFRAME",10,150,280,60,window,LABEL_SUNKENFRAME)
    CreateLabel("not applicable",10,220,280,54,window,LABEL_SEPARATOR)
    
    While WaitEvent()<>EVENT_WINDOWCLOSE
    Wend

See Also
========



