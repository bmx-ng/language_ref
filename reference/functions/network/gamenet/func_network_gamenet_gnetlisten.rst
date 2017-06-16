.. _func_network_gamenet_gnetlisten:

==========
GNetListen
==========

GNetListen - 

Description
===========

.. code-block:: blitzmax

    GNetListen( host:TGNetHost,port )

Listen for connections

Causes @host to start listening for connection attempts on the specified @port.
Once a host is listening, hosts on other machines can connect using #GNetConnect.

#GNetListen may fail if @port is already in use by another application, or if @host
is already listening or has already connected to a remote host using #GNetConnect.

Parameters
==========

Return Values
=============

True if successful, otherwise false

Examples
========

See Also
========



