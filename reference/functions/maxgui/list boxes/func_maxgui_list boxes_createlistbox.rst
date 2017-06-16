.. _func_maxgui_list boxes_createlistbox:

=============
CreateListBox
=============

CreateListBox - 

Description
===========

.. code-block:: blitzmax

    CreateListBox:TGadget(x,y,w,h,group:TGadget,style=0)

Create a ListBox gadget.

A ListBox gadget displays a scrollable list of items and generates the following events:

[ @{Event ID} | @Description
* EVENT_GADGETSELECT | An item has been selected, or the selection has been cleared.
* EVENT_GADGETACTION | An item has been double-clicked.
* EVENT_GADGETMENU | The user has right-clicked somewhere in the listbox.
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

    ' createlistbox.bmx
    
    Strict 
    
    Import MaxGui.Drivers
    
    Local window:TGadget
    Local listbox:TGadget
    
    window=CreateWindow("My Window",30,20,200,200)
    
    Const ETIP$="Great for lovers of rain, mushy peas and stomping beats.~r~nNew line..."
    
    listbox=CreateListBox(4,4,100,80,window)
    
    AddGadgetItem listbox,"German"
    AddGadgetItem listbox,"England",False,-1,ETIP
    AddGadgetItem listbox,"French",False,-1,"tip - goes here","mystringobject"
    
    SelectGadgetItem listbox,2
    
    While WaitEvent()
        Print CurrentEvent.ToString()
        If EventSource()=listbox
            Print "SelectedGadgetItem()="+SelectedGadgetItem(listbox)
            If EventData()<>SelectedGadgetItem(listbox) Print "error with skidracer"
        EndIf
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
        End Select
    Wend

See Also
========



