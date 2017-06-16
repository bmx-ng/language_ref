.. _func_maxgui_redrawgadget:

============
RedrawGadget
============

RedrawGadget - 

Description
===========

.. code-block:: blitzmax

    RedrawGadget( gadget:TGadget )

Redraws a gadget.

The RedrawGadget command causes the gadget to be redrawn by the underlying
Operating System and is not guaranteed to happen immediately.

In the case of a @Canvas gadget an EVENT_GADGETPAINT event is emitted
when the Operating System begins the actual redraw. The following example
illustrates how to manage this feature:

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' redrawgadget.bmx
    
    ' version 2 - improved TApplet behavior
    ' moved AddHook from New to Run, as firing OnEvent
    ' before object has been initialized was problematic
    
    Import MaxGui.Drivers
    
    Strict
    
    Type TApplet 
    
        Method OnEvent(Event:TEvent) Abstract
    
        Method Run()
            AddHook EmitEventHook,eventhook,Self
        End Method
    
        Function eventhook:Object(id,data:Object,context:Object)
            Local    event:TEvent
            Local    app:TApplet
            event=TEvent(data)
            app=TApplet(context)
            app.OnEvent event    
        End Function
    
    End Type
    
    Type TSpinningApplet Extends TApplet
    
        Field    window:TGadget
        Field    canvas:TGadget
        Field    timer:TTimer
        Field    image:TImage
        
        Method Draw()
            SetGraphics CanvasGraphics(canvas)
            SetViewport 0,0,GraphicsWidth(),GraphicsHeight()
            SetBlend ALPHABLEND
            SetRotation MilliSecs()*.1
            SetClsColor 255,0,0
            Cls
            DrawImage image,GraphicsWidth()/2,GraphicsHeight()/2
            Flip
        End Method
        
        Method OnEvent(Event:TEvent)
            Select event.id
            Case EVENT_WINDOWCLOSE
                End
            Case EVENT_TIMERTICK
                RedrawGadget canvas
            Case EVENT_GADGETPAINT
                Draw
            End Select
        End Method
        
        Method Create:TSpinningApplet(name$)
            Local    w,h
            image=LoadImage("fltkwindow.png")
            window=CreateWindow(name,20,20,512,512)
            w=ClientWidth(window)
            h=ClientHeight(window)
            canvas=CreateCanvas(0,0,w,h,window)
            canvas.SetLayout 1,1,1,1
            timer=CreateTimer(100)
            Run
            Return Self        
        End Method
        
    End Type
    
    AutoMidHandle True
    
    Local    spinner:TSpinningApplet
    
    spinner=New TSpinningApplet.Create("Spinning Applet")
    
    While True
        WaitEvent
    Wend

See Also
========



