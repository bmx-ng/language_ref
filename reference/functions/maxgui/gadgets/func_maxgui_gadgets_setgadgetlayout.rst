.. _func_maxgui_gadgets_setgadgetlayout:

===============
SetGadgetLayout
===============

SetGadgetLayout - 

Description
===========

.. code-block:: blitzmax

    SetGadgetLayout( gadget:TGadget,Left,Right,Top,Bottom )

Set the layout rules for a gadget when its parent is resized.

#SetGadgetLayout lets you control the automatic layout of a gadget in the event its parent is resized.

This will happen either if a window is resized, or if #SetGadgetShape is called on a group gadget.

Each edge of a @Gadget has an alignment setting that fixes it in place in the following manner:

[ @Constant | @Description
* EDGE_CENTERED | The edge of the gadget is kept a fixed distance from the center of its parent.
* EDGE_ALIGNED | The edge of the gadget stays a fixed distance from its parent's corresponding edge.
* EDGE_RELATIVE | The edge of the gadget remains a proportional distance from both of its parent's edges.
]

The default behaviour may vary between platforms, so it is highly recommended that you set this for gadgets on resizable windows.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



