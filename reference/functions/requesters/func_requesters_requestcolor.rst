.. _func_requesters_requestcolor:

============
RequestColor
============

RequestColor - 

Description
===========

.. code-block:: blitzmax

    RequestColor(r,g,b)

Prompts the user for a color.

The parameters @red, @green, @blue are the initial color to display in the requester,
with components in the range 0 to 255.

After a color is selected, use the #RequestedRed, #RequestedGreen And #RequestedBlue
functions to determine the color selected by the user.

Parameters
==========

Return Values
=============

#True if a color is selected, #False if the requester was cancelled.

Examples
========

.. code-block:: blitzmax

    ' requestcolor.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    Local panel:TGadget
    Local red,green,blue
    
    window=CreateWindow("RequestColor",40,40,320,240)
    panel=CreatePanel(20,20,32,32,window,PANEL_ACTIVE|PANEL_BORDER)
    
    While True
        WaitEvent 
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
            Case EVENT_MOUSEDOWN
                If RequestColor(red,green,blue)
                    red=RequestedRed()
                    green=RequestedGreen()
                    blue=RequestedBlue()
                    SetPanelColor panel,red,green,blue
                EndIf                
        End Select
    Wend

See Also
========



