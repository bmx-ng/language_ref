.. _func_maxgui_canvases_createcanvas:

============
CreateCanvas
============

CreateCanvas - 

Description
===========

.. code-block:: blitzmax

    CreateCanvas:TGadget(x,y,w,h,group:TGadget,style=0)

Create a Canvas gadget.

A Canvas provides a #Graphics interface for realtime drawing purposes.

Once a Canvas is created, the #CanvasGraphics() Function can be used with the
#SetGraphics command to direct #Max2D drawing commands to be
drawn directly on the Canvas.

An EVENT_GADGETPAINT event is generated whenever the gadget must be redrawn by either
the system (for instance when it is first shown) or due to the #RedrawGadget command.

An EVENT_GADGETPAINT handler should always call #SetGraphics
with the canvas's Max2D graphics context to ensure the viewport and similar
properties are in their correct state.

When a Canvas is active using either the #ActivateGadget command or clicking
on the Canvas when the application is running, the following event's will also
be sent from the Canvas:

[ @{Event ID} | @Description
* EVENT_MOUSEDOWN | Mouse button pressed. Event data contains mouse button code.
* EVENT_MOUSEMOVE | Mouse moved. Event x and y contain mouse coordinates.
* EVENT_MOUSEWHEEL | Mouse wheel spun. Event data contains delta clicks.
* EVENT_MOUSEENTER | Mouse entered gadget area.
* EVENT_MOUSELEAVE | Mouse left gadget area.
* EVENT_KEYDOWN | Key pressed. Event data contains keycode.
* EVENT_KEYUP | Key released. Event data contains keycode.
* EVENT_KEYCHAR | Key character. Event data contains unicode value.
]

See Also: #ActivateGadget, #RedrawGadget, #CanvasGraphics

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createcanvas.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Global GAME_WIDTH=320
    Global GAME_HEIGHT=240
    
    ' create a centered window with client size GAME_WIDTH,GAME_HEIGHT
    
    Local wx=(ClientWidth(Desktop())-GAME_WIDTH)/2
    Local wy=(ClientHeight(Desktop())-GAME_HEIGHT)/2
    
    Local window:TGadget=CreateWindow("My Canvas",wx,wy,GAME_WIDTH,GAME_HEIGHT,Null,WINDOW_TITLEBAR|WINDOW_CLIENTCOORDS)
    
    ' create a canvas for our game
    
    Local canvas:TGadget=CreateCanvas(0,0,320,240,window)
    
    ' create an update timer
    
    CreateTimer 60
    
    While WaitEvent()
        Select EventID()
            Case EVENT_TIMERTICK
                RedrawGadget canvas
    
            Case EVENT_GADGETPAINT
                SetGraphics CanvasGraphics(canvas)
                SetOrigin 160,120
                SetLineWidth 5
                Cls
                Local t=MilliSecs()
                DrawLine 0,0,120*Cos(t),120*Sin(t)
                DrawLine 0,0,80*Cos(t/60),80*Sin(t/60)
                Flip
    
            Case EVENT_MOUSEMOVE
                Print "MOVE!"
    
            Case EVENT_WINDOWCLOSE
                FreeGadget canvas
                End
    
            Case EVENT_APPTERMINATE
                End
        End Select
    Wend

See Also
========



