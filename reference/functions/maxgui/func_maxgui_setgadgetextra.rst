.. _func_maxgui_setgadgetextra:

==============
SetGadgetExtra
==============

SetGadgetExtra - 

Description
===========

.. code-block:: blitzmax

    SetGadgetExtra( gadget:TGadget, extra:Object )

Stores a pointer to a related object, that can later be retrieved using #GadgetExtra.

This function has many uses - you may want to store a custom type instance to the treeview node that
represents it, or you may want to store a hidden string value that represents a gadget's action.

However, it is important to note that this function will result in a pointer being stored to that object
which will only be released when a new object or #Null is passed to this function, or when the gadget is freed
using #FreeGadget.

Parameters
==========

Return Values
=============

Nothing.

Examples
========

See Also
========



