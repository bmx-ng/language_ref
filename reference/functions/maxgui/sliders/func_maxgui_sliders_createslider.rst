.. _func_maxgui_sliders_createslider:

============
CreateSlider
============

CreateSlider - 

Description
===========

.. code-block:: blitzmax

    CreateSlider:TGadget(x,y,w,h,group:TGadget,style=0)

Create a Slider gadget.

A Slider gadget supports the following styles:

[ @Style | @Meaning
* SLIDER_HORIZONTAL | The slider is moved left and right.
* SLIDER_VERTICAL | The  slider is moved up and down.
* SLIDER_SCROLLBAR | The slider uses a proportional size knob.
* SLIDER_TRACKBAR | The slider uses a fixed size knob.
* SLIDER_STEPPER | The slider has no knob, just arrow buttons.
]

A slider only emits one type of event:

[ @{Event ID} | @Description
* EVENT_GADGETACTION | The user has changed the slider's value. Event Data contains the SliderValue.
]

See Also: #SetSliderRange, #SetSliderValue and #SliderValue

Parameters
==========

Return Values
=============

Nothing.

Examples
========

.. code-block:: blitzmax

    ' createslider.bmx
    
    Import MaxGui.Drivers
    
    Strict 
    
    Local window:TGadget=CreateWindow("My Window",0,0,240,240,,WINDOW_TITLEBAR)
    
    Local slider:TGadget[3]
    
    ' standard vertical and horizontal scroll bars
    
    slider[0]=CreateSlider(10,10,16,100,window,SLIDER_VERTICAL)
    slider[1]=CreateSlider(30,10,100,16,window,SLIDER_HORIZONTAL)
    
    ' a horizontal trackbar
    
    slider[2]=CreateSlider(30,30,100,24,window,SLIDER_HORIZONTAL|SLIDER_TRACKBAR)
    
    ' a row of vertical trackbars
    
    Local trackbar:TGadget[5]
    
    For Local i=0 To 4
        trackbar[i]=CreateSlider(30+i*20,50,16,60,window,SLIDER_VERTICAL|SLIDER_TRACKBAR)
    Next
    
    ' a single stepper
    
    Local stepper:TGadget
    stepper=CreateSlider(10,120,24,24,window,SLIDER_STEPPER)
    
    SetSliderValue stepper,4
    Print SliderValue(stepper)
    
    While WaitEvent()
        Print CurrentEvent.ToString()
        Select EventID()
            Case EVENT_WINDOWCLOSE
                End
        End Select
    Wend

See Also
========



