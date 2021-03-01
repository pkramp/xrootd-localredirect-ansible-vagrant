A vagrant setup with a client and server VM. The server runs a fork version of XRootD for testing the cms.localredirect functionality. The client runs a standard xrootd-client, which runs a few different requests, to see if and how root:// and http(s):// requests are handled by the XRootD cms local redirect plug-in.

The provisioning is done via ansible.
