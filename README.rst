Nginx
=====

Configuration
-------------

The supplied :file:`nginx.conf` sets up the appropriate configuration for running
locally out of the repository directory. 

Essentially, requests for static files are handled by `Nginx`_, requests for API endpoints are proxied to port 8081.

Running
-------

.. code:: sh

    nginx -c nginx.conf -p $(pwd)


.. _Nginx: https://www.nginx.com/

Stopping
--------

nginx -s stop
  
Troubleshooting
---------------

https://blog.serverdensity.com/troubleshoot-nginx/