.. _func_maxgui_panels_createpanel:

===========
CreatePanel
===========

CreatePanel - 

Description
===========

.. code-block:: blitzmax

    CreatePanel:TGadget(x,y,w,h,group:TGadget,style=0,title$="")

Create a Panel gadget.

A Panel is a general purpose gadget that can be used to group other gadgets,
it has background color and pixmap properties.

A panel can feature the following optional styles:

[ @Style | @Meaning
* PANEL_BORDER | Panel is drawn with a border.
* PANEL_ACTIVE | Panel generates mouse move events.
* PANEL_GROUP | Panel is drawn with a titled etched border.
]

If the PANEL_ACTIVE style flag is specified, the Panel will emit the following
mouse and key events:

[ @{Event ID} | @Description
* EVENT_MOUSEDOWN | Mouse button pressed. Event data contains mouse button code.
* EVENT_MOUSEUP | Mouse button released. Event data contains mouse button code.
* EVENT_MOUSEMOVE | Mouse moved. Event x and y contain mouse coordinates.
* EVENT_MOUSEWHEEL | Mouse wheel spun. Event data contains delta clicks.
* EVENT_MOUSEENTER | Mouse entered gadget area.
* EVENT_MOUSELEAVE | Mouse left gadget area.
* EVENT_KEYDOWN | Key pressed. Event data contains keycode.
* EVENT_KEYUP | Key released. Event data contains keycode.
* EVENT_KEYCHAR | Key character. Event data contains unicode value.
]

%{Note: The PANEL_BORDER and PANEL_GROUP style flags cannot be used together.}

See Also: #SetPanelColor and #SetPanelPixmap.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createpanel.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Local panel:TGadget
    Local panel2:TGadget
    Local group:TGadget
    
    window=CreateWindow("My Window",40,40,320,240)
    
    ' create a purple panel that occupies entire window client area
    
    panel=CreatePanel(0,0,ClientWidth(window),ClientHeight(window),window,PANEL_ACTIVE)
    SetGadgetLayout panel,1,1,1,1
    'SetPanelColor panel,100,0,200
    
    ' and a smaller box
    
    panel2=CreatePanel(10,10,100,100,panel,PANEL_ACTIVE|PANEL_BORDER)
    panel2.SetColor(160,255,160)
    
    ' and a group panel with a child button
    
    group=CreatePanel(120,10,100,100,panel,PANEL_GROUP)
    group.settext("My Group")
    CreateButton("hello",0,0,64,24,group)
    
    
    While True
        WaitEvent 
        Print CurrentEvent.ToString()
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
        End Select
    Wend

See Also
========



