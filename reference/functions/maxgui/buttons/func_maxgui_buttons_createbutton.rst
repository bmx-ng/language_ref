.. _func_maxgui_buttons_createbutton:

============
CreateButton
============

CreateButton - 

Description
===========

.. code-block:: blitzmax

    CreateButton:TGadget(label$,x,y,w,h,group:TGadget,style=BUTTON_PUSH)

Create a Button gadget.

A Button generates an EVENT_GADGETACTION #TEvent whenever it is pushed.

[ @Style | @Meaning
* BUTTON_PUSH | Standard push button.
* BUTTON_CHECKBOX | A check box button that displays a tick when it's state is #True.
* BUTTON_RADIO | A radio button is accompanied by a small circular indicator, filled when it's state is #True.
* BUTTON_OK | Standard push button that is also activated when the user presses the RETURN key.
* BUTTON_CANCEL | Standard push button that is also activated when the user presses the ESCAPE key.
]

On certain platforms, the BUTTON_PUSH flag can be combined with either BUTTON_CHECKBOX or BUTTON_RADIO to obtain
a button looking similar to standard push-buttons, but mimicking the behaviour of the checkbox or radio button.

See Also: #SetGadgetText, #SetButtonState, #ButtonState and #SetGadgetPixmap.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createbutton.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Global window:TGadget = CreateWindow("MaxGUI Buttons",40,40,400,330,Null,WINDOW_TITLEBAR|WINDOW_CLIENTCOORDS)
        CreateButton("Std. Button",10,10,120,30,window,BUTTON_PUSH)
        CreateButton("OK Button",140,10,120,30,window,BUTTON_OK)
        CreateButton("Cancel Button",270,10,120,30,window,BUTTON_CANCEL)
    
    Global panel:TGadget[4]
        panel[0]=CreatePanel(10,50,380,60,window,PANEL_GROUP,"Checkbox")
            FillPanelWithButtons(panel[0], BUTTON_CHECKBOX, "Checkbox")
        panel[1]=CreatePanel(10,120,380,60,window,PANEL_GROUP,"Checkbox (with Push Button Style)")
            FillPanelWithButtons(panel[1], BUTTON_CHECKBOX|BUTTON_PUSH, "Toggle")
        panel[2]=CreatePanel(10,190,380,60,window,PANEL_GROUP,"Radio Buttons")
            FillPanelWithButtons(panel[2], BUTTON_RADIO, "Option ")
        panel[3]=CreatePanel(10,260,380,60,window,PANEL_GROUP,"Radio Buttons (with Push Button Style)")
            FillPanelWithButtons(panel[3], BUTTON_RADIO|BUTTON_PUSH, "Option")
    
    Repeat
        Select WaitEvent()
            Case EVENT_WINDOWCLOSE, EVENT_APPTERMINATE
                End
            Case EVENT_GADGETACTION
                Print "EVENT_GADGETACTION~n" + ..
                "GadgetText(): ~q" + GadgetText(TGadget(EventSource())) + "~q ~t " + ..
                "ButtonState(): "+ ButtonState(TGadget(EventSource()))
        EndSelect
    Forever
    
    Function FillPanelWithButtons( pPanel:TGadget, pStyle%, pText$ = "Button" )
        Local buttonwidth% = (pPanel.width-10)/3
        For Local i% = 0 Until 3
            CreateButton( pText + " " + (i+1), 5+(i*buttonwidth), 5, buttonwidth-10, 26, pPanel, pStyle )
        Next
    EndFunction

See Also
========



