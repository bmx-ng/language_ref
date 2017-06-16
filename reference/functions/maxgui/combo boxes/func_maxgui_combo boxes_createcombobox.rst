.. _func_maxgui_combo boxes_createcombobox:

==============
CreateComboBox
==============

CreateComboBox - 

Description
===========

.. code-block:: blitzmax

    CreateComboBox:TGadget(x,y,w,h,group:TGadget,style=0)

Create a ComboBox gadget.

A ComboBox gadget provides a dropdown list of items to the user.

The ComboBox supports the following styles:

[ @Style | @Meaning
* COMBOBOX_EDITABLE | Allows the ComboBox to behave similar to a TextField, by allowing typed user input also.
]

And emits the following events:

[ @{Event ID} | @Description
* EVENT_GADGETACTION | An item has been selected, or the selection has been cleared.
]



See Also: #AddGadgetItem, #ClearGadgetItems, #ModifyGadgetItem, #SelectGadgetItem,
#RemoveGadgetItem and #SelectedGadgetItem.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createcombobox.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Local combobox:TGadget
    
    window=CreateWindow("My Window",30,20,200,200)
    
    combobox=CreateComboBox(4,4,120,22,window)
    AddGadgetItem combobox,"Short"
    AddGadgetItem combobox,"Medium"
    AddGadgetItem combobox,"Fat",True
    AddGadgetItem combobox,"Humungous"
    
    While WaitEvent()
        Select EventID()
            Case EVENT_GADGETACTION
                Print "eventdata="+EventData()
            Case EVENT_WINDOWCLOSE
                End
        End Select
    Wend

See Also
========



