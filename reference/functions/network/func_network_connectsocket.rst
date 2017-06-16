.. _func_network_connectsocket:

=============
ConnectSocket
=============

ConnectSocket - 

Description
===========

.. code-block:: blitzmax

    ConnectSocket( socket:TSocket,remoteIp,remotePort )

Connect a socket to a remote ip and port

For both UDP and TCP sockets, #ConnectSocket will fail if the specified
ip address could not be reached.

In the case of TCP sockets, #ConnectSocket will also fail if there is
no application listening at the remote port.

Parameters
==========

Return Values
=============

True if successful, otherwise false

Examples
========

See Also
========



