.. _func_maxgui_sliders_setsliderrange:

==============
SetSliderRange
==============

SetSliderRange - 

Description
===========

.. code-block:: blitzmax

    SetSliderRange(slider:TGadget,range0,range1)

Set the range of a Slider gadget.
For the default SLIDER_SCROLLBAR style the range0,range1 parameters are treated
as a visible / total ratio which dictates both the size of the knob and it's
maximum value. The default value is 1,10 which displays a Slider with a knob
that occupies 1/10th the area and with a #SliderValue range of 0..9.

For the SLIDER_TRACKBAR and SLIDER_STEPPER styles the range0,range1 parameters
are treated as the minimum and maximum #SliderValue range inclusive.

See Also: #CreateSlider, #SliderValue and #SetSliderValue

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



