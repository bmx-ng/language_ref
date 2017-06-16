.. _func_maxgui_toolbars_createtoolbar:

=============
CreateToolBar
=============

CreateToolBar - 

Description
===========

.. code-block:: blitzmax

    CreateToolBar:TGadget(source:Object,x,y,w,h,group:TGadget,style=0)

Create a ToolBar gadget.

A ToolBar is created from a source pixmap that contains a row of equally
shaped images. Any images in the row left blank are treated as ToolBar
separators. A ToolBar generates the following events:

[ @{Event ID} | @Description
* EVENT_GADGETACTION | A toolbar item has been selected/clicked. Event data contains the item index.
]

The recommended image size is 24x24 pixels which seems to work well on all
platforms. Using a different image size may result in the pixmaps being scaled
before being set depending on the OS.

The @source parameter can either be a #TPixmap or a URL to an image
file from which @CreateToolBar loads a pixmap.

See Also: #AddGadgetItem, #EnableGadgetItem, #DisableGadgetItem and #SetToolBarTips.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createtoolbar.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget=CreateWindow("My Window",50,50,480,240)
    
    Local toolbar:TGadget=CreateToolBar("toolbar.bmp",0,0,0,0,window)
    
    SetToolBarTips toolbar,["New","Open","Save~nmy soul"] 
    
    AddGadgetItem toolbar,"hello",GADGETITEM_TOGGLE,2,"This item is a quick test of GADGETITEM_TOGGLE"
    
    DisableGadgetItem toolbar,2
    
    While WaitEvent()
        Select EventID()
            Case EVENT_GADGETACTION
                If EventSource()=toolbar 
                    Print "ToolBar GadgetAction~nEventData()="+EventData()
                EndIf
            Case EVENT_WINDOWCLOSE
                End
        End Select
    Wend

See Also
========



