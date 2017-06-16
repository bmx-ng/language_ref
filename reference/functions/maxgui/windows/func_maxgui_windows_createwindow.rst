.. _func_maxgui_windows_createwindow:

============
CreateWindow
============

CreateWindow - 

Description
===========

.. code-block:: blitzmax

    CreateWindow:TGadget( titletext$,x,y,w,h,group:TGadget=Null,style=15 )

Create a Window gadget.

A Window is the primary gadget of MaxGUI. Windows should be used as the primary
group gadgets in MaxGUI applications to contain the gadgets that make up the program's
user interface.

The following style flags are supported when creating a Window. Any of the
style flags can be combined using the bitwise operator '|'.

[ @Style | @Meaning
* WINDOW_TITLEBAR | The Window has a titlebar that displays the @titletext$.
* WINDOW_RESIZABLE | The Window can be resized by the user.
* WINDOW_MENU | The Window has a menubar (required if you wish to add menus to a Window).
* WINDOW_STATUS | The Window has a statusbar.
* WINDOW_TOOL | The Windows will look and behave like a floating window.
* WINDOW_CLIENTCOORDS | The dimensions specified relate to the client area as opposed to the window frame.
* WINDOW_CENTER | The x and y values are ignored, and the Window is positioned either in the middle of the screen or the middle of the parent gadget.
* WINDOW_HIDDEN | The Window is created in a hidden state and can be revealed later using #ShowGadget.
* WINDOW_ACCEPTFILES | Enable file drag and drop operations (emits the EVENT_WINDOWACCEPT events).
]

Note: For cross-platform projects, it is highly recommended that the WINDOW_CLIENTCOORDS style is used to maintain
similar layouts with different operating systems.

The default window style (15) is equivalent to WINDOW_TITLEBAR | WINDOW_RESIZABLE | WINDOW_MENU | WINDOW_STATUS.

A Window emits the following events:

[ @{Event ID} | @Description
* EVENT_WINDOWMOVE | Window has been moved.
* EVENT_WINDOWSIZE | Window has been resized.
* EVENT_WINDOWCLOSE | Window close icon clicked.
* EVENT_WINDOWACTIVATE | Window activated.
* EVENT_WINDOWACCEPT | A file was dropped onto a Window with the WINDOW_ACCEPTFILES style. The Event Extra object holds the filepath.
]

See Also: #WindowMenu, #UpdateWindowMenu, #PopupWindowMenu, #ActivateWindow, #SetStatusText,
#SetMinWindowSize, #SetMaxWindowSize, #MinimizeWindow, #MaximizeWindow, #RestoreWindow, #WindowMinimized
and #WindowMaximized.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createwindow.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget
    
    window=CreateWindow("My Window",40,40,320,240)
    
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



