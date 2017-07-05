Nginx
=====

Configuration
-------------

Using nginx-light

The supplied ``nginx.conf`` sets up the appropriate configuration for running
locally out of the repository directory. 

Essentially, requests for static files are handled by `Nginx`_, requests for API endpoints are proxied to port 8081.

Running
-------

.. code:: sh

    nginx -c nginx.conf -p $(pwd)


.. _Nginx: https://www.nginx.com/

Stopping
--------

``nginx -s stop``
  
Troubleshooting
---------------

https://blog.serverdensity.com/troubleshoot-nginx/


TODO
----

npm target script
^^^^^^^^^^^^^^^^^
In dev source package.json


``clean-build: rm -rf  nginx-vue/static; rm -rf  nginx-vue/index.html;``

``cp -r <dev-source>/dist/* nginx-vue/``

Size
----

.. code:: sh

    static     385 KB
    index.html   4   KB




    $ tree --du
    .
    ├── [        750]  README.rst
    ├── [        460]  index.html
    ├── [        781]  nginx.conf
    └── [     349165]  static
        ├── [     108722]  css
        │   └── [     108620]  app.6053d03038f2cb9eab4765770a16f8d6.css
        └── [     240307]  js
            ├── [       8602]  0.76f07e34ec770a5edcf0.js
            ├── [      49333]  1.f2de0c733f1dd52060f6.js
            ├── [        709]  2.92fc7b709a85fc82873f.js
            ├── [       5072]  app.84af63ec1bdace2cc4e4.js
            ├── [       1528]  manifest.213078b0cd2cc9b07937.js
            └── [     174791]  vendor.e9060fb6851c507196ba.js

      351428 bytes used in 3 directories, 10 files

Prerquisite
-----------

nginx  `nginx-light`

https://askubuntu.com/questions/553937/what-is-the-difference-between-the-core-full-extras-and-light-packages-for-ngi

https://packages.debian.org/sid/nginx-light
