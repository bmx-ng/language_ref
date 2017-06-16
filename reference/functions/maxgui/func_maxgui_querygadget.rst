.. _func_maxgui_querygadget:

===========
QueryGadget
===========

QueryGadget - 

Description
===========

.. code-block:: blitzmax

    QueryGadget(gadget:TGadget,queryid)

Return internal gadget properties.
Dependent on the Operating System and type of Gadget, #QueryGadget
can be used to retrieve system handles useful for programming platform
specific functions that extend the functionality of a TGadget.

[ @Constant | @Return Value
* QUERY_HWND | A Windows API HWND handle.
* QUERY_HWND_CLIENT | A Windows API HWND handle representing a gadget's client area.
* QUERY_NSVIEW | A Cocoa NSView handle.
* QUERY_NSVIEW_CLIENT | A Cocoa NSView representing a gadget's client area.
* QUERY_FLWIDGET | An FL_WIDGET handle.
* QUERY_FLWIDGET_CLIENT | An FL_WIDGET handle representing a gadget's client area.
]

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    Strict
    
    Import MaxGUI.Drivers
    Import MaxGUI.ProxyGadgets
    
    AppTitle = "Hyperlink Test Window"
    
    Global wndMain:TGadget = CreateWindow( AppTitle, 100, 100, 300, 59, Null, WINDOW_TITLEBAR|WINDOW_CLIENTCOORDS|WINDOW_STATUS )
        
        'Standard Hyperlink Gadget
        Global hypLeft:TGadget = CreateHyperlink( "http://www.blitzbasic.com/", 2, 2, ClientWidth(wndMain)-4, 15, wndMain, LABEL_LEFT )
        
        'Center Aligned Hyperlink Gadget with alternate text
        Global hypCenter:TGadget = CreateHyperlink( "http://www.blitzbasic.com/", 2, 21, ClientWidth(wndMain)-4, 17, wndMain, LABEL_CENTER|LABEL_FRAME, "Alternate Text" )
        
        'Right Aligned Sunken Hyperlink Gadget with custom rollover colors set
        Global hypRight:TGadget = CreateHyperlink( "http://www.blitzbasic.com/", 2, 42, ClientWidth(wndMain)-4, 15, wndMain, LABEL_RIGHT, "Custom Rollover Colors" )
            SetGadgetTextColor(hypRight,128,128,128)    'Set normal text color to grey.
            SetGadgetColor(hypRight,255,128,0)            'Set rollover color to orange.
    
    Repeat
        
        WaitEvent()
        
        SetStatusText wndMain, CurrentEvent.ToString()
        
        Select EventID()
            Case EVENT_WINDOWCLOSE, EVENT_APPTERMINATE
    End
        EndSelect
        
    Forever

See Also
========



