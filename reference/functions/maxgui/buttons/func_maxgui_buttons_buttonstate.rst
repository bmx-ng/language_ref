.. _func_maxgui_buttons_buttonstate:

===========
ButtonState
===========

ButtonState - 

Description
===========

.. code-block:: blitzmax

    ButtonState( button:TGadget )

Retrieve a Button's state.

Returns a non-zero value if a checkbox or radio button is selected or false if it isn't.
On certain platforms, if a checkbox is set using #SetButtonState to have an indeterminant
state (CHECK_INDETERMINATE), then this function will return CHECK_INDETERMINATE too.
See Also: #CreateButton, #SetGadgetText, #SetButtonState and #SetGadgetPixmap.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



