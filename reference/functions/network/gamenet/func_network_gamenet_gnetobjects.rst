.. _func_network_gamenet_gnetobjects:

===========
GNetObjects
===========

GNetObjects - 

Description
===========

.. code-block:: blitzmax

    GNetObjects:TList( host:TGNetHost,state=GNET_ALL )

Get a list of GNet objects

#GNetObjects returns a list of GNet objects in a certain state.

The @state parameter controls which objects are listed, and can be one of &GNET_ALL,
&GNET_CREATED, &GNET_MODIFIED or &GNET_CLOSED.

Note that with the exception of &GNET_ALL, the returned lists will only ever contain remote objects.

Parameters
==========

Return Values
=============

A linked list

Examples
========

See Also
========



