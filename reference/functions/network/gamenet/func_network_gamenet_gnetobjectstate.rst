.. _func_network_gamenet_gnetobjectstate:

===============
GNetObjectState
===============

GNetObjectState - 

Description
===========

.. code-block:: blitzmax

    GNetObjectState( obj:TGNetObject )

Get state of a GNet object
The returned value can be one of the following:
<table>
<tr><th>Object State</th><td>Meaning</td></tr>
<tr><td>GNET_CREATED</td><td>Object has been created</td></tr>
<tr><td>GNET_SYNCED</td><td>Object is in sync</td><tr>
<tr><td>GNET_MODIFIED</td><td>Object has been modified</td></tr>
<tr><td>GNET_CLOSED</td><td>Object has been closed</td></tr>
<tr><td>GNET_ZOMBIE</td><td>Object is a zombie</td></tr>
<tr><td>GNET_MESSAGE</td><td>Object is a message object</td></tr>
</table>
Zombie objects are objects that have been successfully closed and will never again be used
by GameNet. Therefore, such objects will never appear in any list returned by the
#GNetObjects function.

Parameters
==========

Return Values
=============

An integer state

Examples
========

See Also
========



