.. _func_network_bindsocket:

==========
BindSocket
==========

BindSocket - 

Description
===========

.. code-block:: blitzmax

    BindSocket( socket:TSocket,localPort )

Bind a socket to a local port

If @localPort is 0, a new local port will be allocated. If @localPort is not 0,
#BindSocket will fail if there is already an application bound to @localPort.

Parameters
==========

Return Values
=============

True if successful, otherwise false

Examples
========

See Also
========



